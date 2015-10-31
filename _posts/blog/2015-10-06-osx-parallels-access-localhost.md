---
layout: post
title: OS X에서 Paralles Windows 10 VM의 localhost 사이트에 접속하는 방법
date: 2015-10-06 15:30:31 +9:00 GMT
categories:
  - Another Code
tags:
  - OSX
  - 페러렐즈
  - localhost
  - 호스팅
  - hosting
---

## 개요

Mac에서 Paralles환경의 Windows 10 VM을 이용해 Web API 서버 모듈을 개발하고 있다. 개발환경은 Visual Studio ASP.NET이며, 디버깅을 위해 `http://localhost:60000` 이라는 주소를 이용한다. 클라이언트는 Mac(OS X 10.11)에서 개발하며 그 테스트를 위해 Mac에서 VM내부에 있는 localhost 주소에 접속할 필요가 있다. 처음엔 그냥 간단히 생각했는데, 몇 가지 번거로운 작업이 필요했다.

## 페러렐즈 설정

VM 메뉴에서 Network Device를 `Shared Network`로 해준다. Paralles 11에 windows10 설치하면 기본값이 Shared로 되어 있다. `Shared Network`로 설정하면 IP 10.211.55.0을 subnet으로 하는 DHCP가 구성되어 10.211.55.1에서 10.222.55.254사이의 IP를 부여 받게 된다. 정확한 Windows VM의 IP는 cmd.exe를 실행하여 `ipconfig` 명령으로 확인 할 수 있다.

<pre>
C:\WINDOWS\system32>ipconfig

Windows IP 구성


이더넷 어댑터 이더넷:

   연결별 DNS 접미사. . . . : localdomain
   IPv6 주소 . . . . . . . . . : fdb2:2c26:f4e4:0:84fa:ade8:cfd6:6cc5
   임시 IPv6 주소. . . . . . . : fdb2:2c26:f4e4:0:7ca7:2911:4e75:2037
   링크-로컬 IPv6 주소 . . . . : fe80::84fa:ade8:cfd6:6cc5%7
   IPv4 주소 . . . . . . . . . : <mark>10.211.55.3</mark>
   서브넷 마스크 . . . . . . . : 255.255.255.0
   기본 게이트웨이 . . . . . . : 10.211.55.1

터널 어댑터 isatap.localdomain:

   미디어 상태 . . . . . . . . : 미디어 연결 끊김
   연결별 DNS 접미사. . . . : localdomain

터널 어댑터 Teredo Tunneling Pseudo-Interface:

   연결별 DNS 접미사. . . . :
   IPv6 주소 . . . . . . . . . : 2001:0:9d38:6ab8:340d:19e2:f52c:c8fc
   링크-로컬 IPv6 주소 . . . . : fe80::340d:19e2:f52c:c8fc%9
   기본 게이트웨이 . . . . . . :</pre>

## 호스트 추가

페러렐즈의 ip를 맥의 host파일에 추가하기 위해 nano editor를 사용하여 host파일을 편집한다.

<pre>
$ sudo nano /etc/hosts</pre>

아래 <mark>마킹</mark>된 부분과 같이 IP와 별도의 호스트명을 추가한다. Mac에서 `localhost`를 사용하지 않는다면 주석처리 하고 localhost를 사용해도 되겠다.

<pre>
##
# Host Database
#
# localhost is used to configure the loopback interface
# when the system is booting.  Do not change this entry.
##
127.0.0.1       localhost
255.255.255.255 broadcasthost
::1             localhost
<mark>10.211.55.3     winlocal</mark></pre>

## 방화벽 설정

Windows VM의 방화벽에 인바운드 TCP 60000 포트를 추가해 준다.(자세한 설명은 생략)

## URL 예약

URL예약이라는 표현이 맞는지 모르겠지만 아래와 같이 cmd.exe창에서 netsh의 aclr옵션으로 ACL룰을 추가한다. 이 작업을 위해서는 관리자 권한으로 cmd.exe를 실행해야 한다.

<pre>
C:\WINDOWS\system32>netsh http add urlacl url=http://*:60000/ user={사용자아이디}

URL 예약을 성공적으로 추가했습니다.</pre>

## IIS Express 설정

만약 IIS Express를 사용한다면 applicationhost.config파일의 site태그에 binding설정을 추가해 준다. Visual Studio를 사용한다면 솔루션 폴더의 .vs/config폴더 안에 있다.
VS가 아니면, `Documents\IISExpress\config`폴더에 있다.

<pre class="pretty-print">
&lt;site name=&quot;Wapi.Api(1)&quot; id=&quot;4&quot;&gt;
    &lt;application path=&quot;/&quot; applicationPool=&quot;Clr4IntegratedAppPool&quot;&gt;
        &lt;virtualDirectory path=&quot;/&quot; physicalPath=&quot;\\Mac\Home\Codes\GitHub\wapi\wapi.Api&quot; /&gt;
    &lt;/application&gt;
    &lt;bindings&gt;
      &lt;binding protocol=&quot;http&quot; bindingInformation=&quot;*:60000:localhost&quot; /&gt;
      <mark>&lt;binding protocol=&quot;http&quot; bindingInformation=&quot;*:60000:*&quot; /&gt;</mark>
    &lt;/bindings&gt;
&lt;/site&gt;
</pre>


## 참조

* [https://gist.github.com/justingarrick/6322779](https://gist.github.com/justingarrick/6322779)
