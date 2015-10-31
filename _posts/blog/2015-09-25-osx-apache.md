---
layout: post
title: OS X(10.11)에서 아파치웹서버 구동하기 (Virtual Hosting 구현)
date: 2015-09-25 09:30:31 +9:00 GMT
categories:
  - Another Code
tags:
  - OSX
  - 아파치
  - apache
  - webserver
  - 웹서버
  - virtualhost
---

#### 업데이트 2015-10-01
* OS X를 11(엘 캐피탄)으로 업데이트 했더니 기존에 설정했던 `httpd.conf`파일이 초기화 되어 버렸다.
* `httpd-vhosts.conf`파일은 유지 되는게 이상하다.

## 들어가며

요세미티에는 아파치웹 서버가 설치되어 있다. 버전을 확인해 보면 아래와 같다.

<pre>
$ sw_vers
ProductName:    Mac OS X
ProductVersion: 10.10.5
BuildVersion:   14F27

$ apachectl -v
Server version: Apache/2.4.16 (Unix)
Server built:   Jul 22 2015 21:03:09</pre>

이 웹 서버를 구동하는 방법과 웹 사이트 개발 테스트등 목적을 위해 가상호스팅(Virtual Hosting)을 하는 방법을 기록한다.

## dnsmasq

이 툴은 서브도메인에 와일드카드 사용을 가능하게 해준다. 뿐만아니라 폴더이름을 호스트이름과 매핑시켜주는 기능도 있기 때문에 여러개 사이트를 동시에 개발할때 유용하게 사용할 수 있다.

예를 들어 `~/Sites/client1` 이라는 폴더를 만들기만 하면 별도로 설정파일을 수정하거나 아파치서버를 재시작하지 않아도 즉시 독립된 사이트인 `http://client.dev`와 같은 형식의 접근이 가능하다.

`brew`로 설치 한다.

<pre>
$ brew install dnsmasq
==&gt; Downloading https://homebrew.bintray.com/bottles/dnsmasq-2.75.yosemite.bottle.tar.gz
######################################################################## 100.0%
==&gt; Pouring dnsmasq-2.75.yosemite.bottle.tar.gz
==&gt; Caveats
To configure dnsmasq, copy the example configuration to /usr/local/etc/dnsmasq.conf
and edit to taste.

  cp /usr/local/opt/dnsmasq/dnsmasq.conf.example /usr/local/etc/dnsmasq.conf

To have launchd start dnsmasq at startup:
  sudo cp -fv /usr/local/opt/dnsmasq/*.plist /Library/LaunchDaemons
  sudo chown root /Library/LaunchDaemons/homebrew.mxcl.dnsmasq.plist
Then to load dnsmasq now:
  sudo launchctl load /Library/LaunchDaemons/homebrew.mxcl.dnsmasq.plist
==&gt; Summary
🍺  /usr/local/Cellar/dnsmasq/2.75: 7 files, 512K</pre>

이제 아래 명령들을 아무생각없이 순서대로 실행해 준다. dnsmasq를 위한 설정 작업이며, 기본적으로 .dev로 마무리되는 도메인을 사용하도록 설정한다.

<pre>
$ echo 'address=/.dev/127.0.0.1' > /etc/dnsmasq.conf

$ sudo cp -v $(brew --prefix dnsmasq)/homebrew.mxcl.dnsmasq.plist /Library/LaunchDaemons

$ sudo launchctl load -w /Library/LaunchDaemons/homebrew.mxcl.dnsmasq.plist

$ sudo mkdir /etc/resolver

$ sudo bash -c 'echo "nameserver 127.0.0.1" > /etc/resolver/dev'</pre>

## 아파치(Apache)

요세미티에는 아파치 v2.4가 설치되어 있다.
우선 아파치를 실행해 보면 http://localhost 사이트가 자동으로 구동된다. 사이트에 들어가보면 `It works!`라는 문구가 보인다.

<pre>
$ sudo apachectl start

$ curl http://localhost
&lt;html&gt;&lt;body&gt;&lt;h1&gt;It works!&lt;/h1&gt;&lt;/body&gt;&lt;/html&gt;
</pre>

이 사이트를 구성하는 파일은 아파치 웹서버 설정 파일인 `httpd.conf`의 DocumentRoot에 설정된 디렉토리에 있다. 웹사이트 디렉토리 위치의 기본값은 `"/Library/WebServer/Documents"`로 되어 있다. 

## httpd.conf

1. 아파치 서버 설정파일인 httpd.conf 파일을 수정해 준다. 아래에 나오는 line number OS버전 또는 아파치 버전에 따라 다를수 있다. 

    텍스트 파일 편집을 위해 nano를 사용하여 httpd.conf파일을 연다.

    <pre>
    $ sudo nano /etc/apache2/httpd.conf</pre>

2. 서버파일 시스템에 접근이 가능하도록 하기 위해 아래 지시자 부분을 모두 주석 처리 해준다. (line number : 220 ~ 223)

    <pre>
    #&lt;Directory /&gt;
    #    AllowOverride none
    #    Require all denied
    #&lt;/Directory&gt;</pre>

3. `mod_vhost_alias`모듈을 로드하도록 주석을 제거한다. (line number : 160)

    <pre>
    LoadModule vhost_alias_module libexec/apache2/mod_vhost_alias.so</pre>

4. 가상호스팅 설정을 위해 가상호스트 설정 파일을 include 부분의 주석을 제거한다. (line number : 500)

    <pre>
    # Virtual hosts
    Include /private/etc/apache2/extra/httpd-vhosts.conf
    </pre>

## httpd-vhosts.conf

1. 가상호스트 설정 파일인 httpd-vhosts.conf 파일의 내용을 모두 지우고 아래와 같이 바꿔준다. `onlydel`부분은 본인의 userid로 바꿔주면 된다.

    이 파일도 nano로 수정해 보자. 파일은 아파치폴더내에 extra폴더에 있다.
    
    <pre>
    $ sudo nano /etc/apache2/extra/httpd-vhosts.conf</pre>

    <pre>
    ...
    &lt;Directory &quot;/Users/<mark>onlydel</mark>/Sites&quot;&gt;
        Options Indexes MultiViews FollowSymLinks
        AllowOverride All
        Order allow,deny
        Allow from all
    &lt;/Directory&gt;

    &lt;Virtualhost *:80&gt;
        VirtualDocumentRoot &quot;/Users/<mark>onlydel</mark>/Sites/%1/wwwroot&quot;
        ServerName sites.dev
        ServerAlias *.dev
        UseCanonicalName Off
    &lt;/Virtualhost&gt;
    ...
    </pre>

2. 설정파일을 수정한 다음에는 아파치서버를 재시작해 준다.

    <pre>
    $ sudo apachectl restart</pre>

    혹시 서버가 정상적으로 실행 될 수 있는지 테스트 하려면 -t 옵션을 써준다.

    <pre>
    $ sudo apachectl -t</pre>

    오류가 있다면 아래와 같이 메시지를 보여준다.

    <pre>
    $ sudo apachectl -t
    AH00526: Syntax error on line 45 of /private/etc/apache2/extra/httpd-vhosts.conf:
    format string must be an absolute path, or 'none'</pre>

3. 이제 실제 폴더를 만들어 테스트해보자. 아래와 같이 Site1, Site2 폴더를 각각 만들고 wwwroot폴더에 index.html파일을 만들어 넣은 다음 http://Site1.dev 와 http://Site2.dev 를 브라우저에서 접속해보자.
    <pre>
    $ mkdir -p ~/Sites/Site1Site1/wwwroot
    $ sudo echo '&lt;html&gt;&lt;body&gt;Test Site1&lt;/body&gt;&lt;/html&gt;' &gt; ~/Sites/Site1/wwwroot/index.html

    $ mkdir -p ~/Sites/Site2/wwwroot
    $ sudo echo '&lt;html&gt;&lt;body&gt;Test Site2&lt;/body&gt;&lt;/html&gt;' &gt; ~/Sites/Site2/wwwroot/index.html</pre>

## http://localhost:8099

만약 제목과 같이 localhost에 포트만 8099인 사이트를 호스팅하려면 dnsmasq와는 별개로 `httpd.conf`파일과 `httpd-vhost.conf`파일을 수정해 주면 된다.

1. httpd.conf
    
    nano로 편집하기 위해 아래 명령 실행
    
    <pre>
    $ sudo nano /etc/apache2/httpd.conf</pre>

    `Listen` 부분을 찾아서 사용할 포트를 추가해 준다.

    <pre>
    ...
    #
    # Listen: Allows you to bind Apache to specific IP addresses and/or
    # ports, instead of the default. See also the <VirtualHost>
    # directive.
    #
    # Change this to Listen on specific IP addresses as shown below to
    # prevent Apache from glomming onto all bound IP addresses.
    #
    #Listen 12.34.56.78:80
    Listen 80
    Listen 8088
    Listen 8099
    ...</pre>

2. httpd-vhosts.conf
    
    nano로 편집하기 위해 아래 명령 실행
    
    <pre>
    $ sudo nano /etc/apache2/extra/httpd-vhosts.conf</pre>

    가상호스트를 위해 &lt;virtualhost&gt;부분 추가, `onlydel`부분은 본인의 userid로 변경

    <pre>
      &lt;Virtualhost *:8099&gt;
        VirtualDocumentRoot &quot;/Users/<mark>onlydel</mark>/Sites/localhost8099&quot;
        ServerName localhost
        UseCanonicalName Off
      &lt;/Virtualhost&gt;</pre>

    이제 `/Users/onlydel/Sites/localhost8099`폴더가 사이트의 root경로가 된다. 이 폴더에 index.html이 있으면 `http://localhost:8099/index.html`로 접근할 수 있다.

## 결론

java 컨테이너가 필요한 개발이라면 당연히 tomcat이나 jetty같은 servlet engine이 있어야 겠지만, PHP나 Python같은 개발은 아파치의 가상서버 구축만으로 가능하다. 특히 front-end library 개발하거나 테스트용으로는 충분하다.


## 참조

[https://mallinson.ca/osx-web-development/](https://mallinson.ca/osx-web-development/)
