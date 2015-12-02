---
layout: post
title: aws-ec2-amazon linux-nodejs
date:   2015-11-20 13:24:23 +9:00 GMT
categories: 
  - Javascript
tags: 
  - nodejs
  - aws
  - ec2
  - git
  - javascript
---


## 개요

AWS EC2(Elastic Compute Cloud)에 Node를 설치하고 웹 사이트를 서비스해 보기로 한다. 이 글에서는 설치과정과 간단한 샘플 페이지를 테스트 하는것 까지만 다룬다. 

소스코드의 배포는 Git을 이용해서 GitHub 저장소에 올리고 서버에서 다시 패치하는 방식으로 한다.(잘 될지 모르겠지만....)

## AWS EC2

AWS를 알게된지 얼마되진 않았지만 한글로된 도움말들과 많은 Document resource들을 통해 기초적인 내용은 쉽게 익힐수 있었다.

##### EC2 인스턴스 만들기

AWS에 EC2 인스턴스를 새로 만드는 것은 어렵지 않다. [Amazon EC2 도움말](https://docs.aws.amazon.com/ko_kr/AWSEC2/latest/UserGuide/Instances.html?console_help=true){:target="_blank"}참조.

EC2는 기본적으로 AMI(Amazon Machine Images)를 이용해서 가상컴퓨팅 클라우드 서비스를 제공한다.
Linux에 대해서는 잘 모르지만, Amazon Linux AMI를 이용하기로 한다.

AMI는 내가 원하는 머신 이미지를 미리 만들어 놓을 수도 있는데, node 등 라이브러리 설치후 설치된 상태를 이미지로 떠 놓으면 나중에 비슷한 유형의 머신을 동작시키고자 할 때 유용할 것 같다.(흥미진진 하구만...ㅋ)

인스턴스를 만들때 보안그룹(Security Group)을 선택하거나 새로 만들어야 하는데, node 테스트를 위해 TCP 8080포트를 추가 해야 한다. 보안그룹은 인스턴스를 만들때 추가하거나 이미 만들어진 보안그룹을 선택 한다. 나중에 변경하는 방법은 아직 찾지 못했다. 그러니 인스턴스 만들때 설정해야 한다. 물론 방법이 있을 거라 생각한다.


##### EC2 접속

PuTTY 같은 SSH 클라이언트 애플리케이션을 이용하거나 터미널에서 직접 SSH로 접속 한다. EC2 Dashboard에서 인스턴스를 선택한 다음 Connect버튼을 클릭하면 ssh 접속 명령이 있다. 복사해서 콘솔에 붙여 넣고 실행 하면 된다. 이때 프라이빗 키 파일(.pem)이 있는 폴더 내에서 실행 하면 제공되는 명령문을 수정할 필요없이 실행할 수 있다. Connect 명령은 아래 마킹된 부분처럼 생겼다.

<pre>
nlydel-MacBook-Pro:aws onlydel$ <mark>ssh -i "aws-realgrid-key.pem" ec2-user@00.000.00.000</mark>
The authenticity of host '00.000.00.000 (00.000.00.000)' can't be established.
ECDSA key fingerprint is SHA256:AxWLj5bMcBKQGoDMkyyMR24F0ahVWxDd6q8Y.
Are you sure you want to continue connecting (yes/no)? y
Please type 'yes' or 'no': yes
Warning: Permanently added '00.000.00.000' (ECDSA) to the list of known hosts.

       __|  __|_  )
       _|  (     /   Amazon Linux AMI
      ___|\___|___|

https://aws.amazon.com/amazon-linux-ami/2015.09-release-notes/
-bash: warning: setlocale: LC_CTYPE: cannot change locale (UTF-8): No such file or directory
[ec2-user@ip- ~]$</pre>

##### 업데이트 Amazon Linux

SSH에 연결하면 우선 Linux 업데이트를 실행한다. AMI의 Linux버전에 따라 많은 양의 업데이트가 이루어지기도 하고 업데이트할 내용이 없기도 한 것 같다. 이런 내용이 확실치 않지만 보안이나 버그패치를 위해 업데이트는 해야 한다고 한다.

## 설치

##### Node.js설치

compiler, ssl, git설치하고 nodejs 저장소를 clone한다.
Node.js는 최근(2015년 5월 부터) NodeJs 재단이 만들어지면서 혼탁했던 node.js와 io.js의 릴리즈들이 통합된듯 하다. [nodejs.org](https://nodejs.org/en/foundation/){:target="_blank"} 

저장소 위치도 joyent에서 nodejs쪽을 이동되었다.[관련내용](https://github.com/nodejs/node-v0.x-archive){:target="_blank"} 

<pre>
[ec2-user@ip- ~]$ sudo yum install gcc-c++ make
[ec2-user@ip- ~]$ sudo yum install openssl-devel
[ec2-user@ip- ~]$ sudo yum install git
[ec2-user@ip- ~]$ git clone https://github.com/nodejs/node.git</pre>

2015년 11월 20일 현재 4.2.2 LTS 가 릴리즈 되었으니 이걸로 설치해 보자.

아래 마킹된 명령을 차례로 실행하여 설치를 진행한다. `git tag -l`은 버전을 확인하기 위한 git명령이다.


<pre>
[ec2-user@ip-1 ~]$ <mark>cd node</mark>
[ec2-user@ip-1 node]$ <mark>git tag -l</mark>
...
v4.1.2
v4.2.0
v4.2.1
v4.2.2
v4.2.2-rc.1
v4.2.2-rc.2
v5.0.0
v5.0.0-rc.1
v5.0.0-rc.2
v5.1.0
[ec2-user@ip-1 node]$ <mark>git checkout v4.2.2</mark>
Note: checking out 'v4.2.2'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by performing another checkout.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -b with the checkout command again. Example:

  git checkout -b &lt;new-branch-name&gt;

HEAD is now at bcf6ac1... 2015-11-03, Version 4.2.2 "Argon" (LTS) Release
[ec2-user@ip-1 node]$ <mark>./configure</mark>
creating  ./icu_config.gypi
{ 'target_defaults': { 'cflags': [],
                       'default_configuration': 'Release',
                       'defines': [],
                       'include_dirs': [],
                       'libraries': []},
  'variables': { 'asan': 0,
                 'gas_version': '2.23',
                 'host_arch': 'x64',
                 'icu_small': 'false',
                 'node_byteorder': 'little',
                 'node_install_npm': 'true',
                 'node_prefix': '/usr/local',
                 'node_release_urlbase': '',
                 'node_shared_http_parser': 'false',
                 'node_shared_libuv': 'false',
                 'node_shared_openssl': 'false',
                 'node_shared_zlib': 'false',
                 'node_tag': '',
                 'node_use_dtrace': 'false',
                 'node_use_etw': 'false',
                 'node_use_lttng': 'false',
                 'node_use_openssl': 'true',
                 'node_use_perfctr': 'false',
                 'openssl_fips': '',
                 'openssl_no_asm': 0,
                 'python': '/usr/bin/python',
                 'target_arch': 'x64',
                 'uv_parent_path': '/deps/uv/',
                 'uv_use_dtrace': 'false',
                 'v8_enable_gdbjit': 0,
                 'v8_enable_i18n_support': 0,
                 'v8_no_strict_aliasing': 1,
                 'v8_optimized_debug': 0,
                 'v8_random_seed': 0,
                 'v8_use_snapshot': 1,
                 'want_separate_host_toolset': 0}}
creating  ./config.gypi
creating  ./config.mk
[ec2-user@ip-1 node]$ <mark>make</mark>
...
...
Release/obj.target/deps/uv/libuv.a /home/ec2-user/node/out/Release/obj.target/deps/v8/tools/gyp/libv8_base.a /home/ec2-user/node/out/Release/obj.target/deps/v8/tools/gyp/libv8_libbase.a /home/ec2-user/node/out/Release/obj.target/deps/v8/tools/gyp/libv8_nosnapshot.a -Wl,--end-group -ldl -lrt -lm
  touch /home/ec2-user/node/out/Release/obj.target/node_dtrace_header.stamp
  touch /home/ec2-user/node/out/Release/obj.target/node_dtrace_provider.stamp
  touch /home/ec2-user/node/out/Release/obj.target/node_dtrace_ustack.stamp
  touch /home/ec2-user/node/out/Release/obj.target/node_etw.stamp
  touch /home/ec2-user/node/out/Release/obj.target/node_perfctr.stamp
  touch /home/ec2-user/node/out/Release/obj.target/specialize_node_d.stamp
make[1]: Leaving directory `/home/ec2-user/node/out'
ln -fs out/Release/node node
[ec2-user@ip-1 node]$ <mark>sudo make install</mark>
make -C out BUILDTYPE=Release V=1
make[1]: Entering directory `/home/ec2-user/node/out'
make[1]: Nothing to be done for `all'.
make[1]: Leaving directory `/home/ec2-user/node/out'
ln -fs out/Release/node node
/usr/bin/python tools/install.py install '' '/usr/local'
installing /usr/local/bin/node
...
...
installing /usr/local/include/node/openssl/archs/solaris64-x86_64-gcc/opensslconf.h
installing /usr/local/include/node/openssl/archs/aix64-gcc/opensslconf.h
installing /usr/local/include/node/openssl/archs/VC-WIN32/opensslconf.h
installing /usr/local/include/node/openssl/opensslconf.h
installing /usr/local/include/node/zconf.h
installing /usr/local/include/node/zlib.h</pre>

node.js와 npm설치를 확인한다. 요즘은 node 설치하면 npm같이 설치되는 건가? 아니면 AMI에 설치된 상태인건가? 아니지 그럼 local에 설치되지 않았겠지? 어쨌거나...

<pre>
[ec2-user@ip-1 ~]$ <mark>node -v</mark>
4.2.2
[ec2-user@ip-1 ~]$ <mark>npm -v</mark>
2.14.7</pre>

패키지 설치 할때 npm을 sudo로 실행 할 수 있도록 /etc/sudoers 파일에 secure_path에 /usr/local/bin경로를 추가해 준다. 

<pre>
[ec2-user@ip-1 ~]$ <mark>sudo nano /etc/sudoers</mark>
...
Defaults    secure_path = /sbin:/bin:/usr/sbin:/usr/bin:/usr/local/bin
...</pre>

시험삼아 express를 global로 설치해 본다.
<pre>
[ec2-user@ip-1 local]$ <mark>sudo npm install express -g</mark>
express@4.13.3 /usr/local/lib/node_modules/express
├── escape-html@1.0.2
├── merge-descriptors@1.0.0
├── cookie@0.1.3
├── array-flatten@1.1.1
├── cookie-signature@1.0.6
├── utils-merge@1.0.0
├── content-type@1.0.1
├── methods@1.1.1
├── vary@1.0.1
├── content-disposition@0.5.0
├── fresh@0.3.0
├── range-parser@1.0.3
├── etag@1.7.0
├── path-to-regexp@0.1.7
├── serve-static@1.10.0
├── parseurl@1.3.0
├── depd@1.0.1
├── qs@4.0.0
├── on-finished@2.3.0 (ee-first@1.1.1)
├── finalhandler@0.4.0 (unpipe@1.0.0)
├── proxy-addr@1.0.8 (forwarded@0.1.0, ipaddr.js@1.0.1)
├── debug@2.2.0 (ms@0.7.1)
├── send@0.13.0 (destroy@1.0.3, statuses@1.2.1, ms@0.7.1, mime@1.3.4, http-errors@1.3.1)
├── accepts@1.2.13 (negotiator@0.5.3, mime-types@2.1.7)
└── type-is@1.6.9 (media-typer@0.3.0, mime-types@2.1.7)</pre>

## 개발 & 배포

개발은 당연히 로컬에서 해야겠지? 물론 vi나 nano같은 터미널 기반 편집기들을 잘 다루는 사람이라면 몰라도...

로컬에서 개발하고 git을 통해 GitHub 저장소로 소스를 올리고 서버에서 다운받는 방법으로 개발과 배포를 진행 한다.

요약하면 ...

* 내 맥에 로컬 폴더를 만들고(윈도우라고 다를것 없지만)
* `npm install express`로 express설치하고
* app.js 파일 만들고 아래 코드로 저장하고
  
  <pre class="prettyprint">
  var http = require('http');
  var express = require('express');

  var app = express();
  var db;

  app.get('/', function(req, res){
    res.send("Hello, World!");
  });

  app.use(function(err, req, res, next){
    if (req.xhr) {
      res.send(500, 'Something went wrong!');
    }
    else {
      next(err);
    }
  });

  console.log('starting the Express (NodeJS) Web server');
  app.listen(8080);
  console.log('Webserver is listening on port 8080');
  </pre>

* GitHub에 올리고
  - `git add -m `
  - `git commit 'init'`
  - `git push origin master`
* 서버로 접속해서 GitHub에서 다운로드
  - `git clone https://github.com/yourid/path:..`
  - `git pull`
* node 실행 
  - `node app.js`
  
  <pre>
  [ec2-user@ip-172-31-21-99 aws-example-nodejs]$ node app.js
  starting the Express (NodeJS) Web server
  Webserver is listening on port 8080</pre>

* 브라우저에서 aws 인스턴스의 public-dns나 public-ip에 8080포트로 접속해 본다. Hello, World!가 보이면 성공.

---
**참조**

* [Amazon EC2 도움말](https://docs.aws.amazon.com/ko_kr/AWSEC2/latest/UserGuide/Instances.html?console_help=true){:target="_blank"}