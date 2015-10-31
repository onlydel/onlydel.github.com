---
layout: post
title: OS X(10.11)에서 MongoDB
date: 2015-10-02 09:30:31 +9:00 GMT
categories:
  - Another Code
tags:
  - OSX
  - 몽고디비
  - mongodb
---

## 들어가며

## 이론

### database

### collection

### document

## 설치

HomeBrew로 설치한다. 만약 /usr/local/bin에 권한이 없다면 write권한을 준다.

<pre>
$ brew install mongodb</pre>

### 수동설치

혹시, 여러가지 이유로 HomeBrew로 설치가 안될 경우 직접 다운로드 받아 설치할 수도 있다. [링크 참조](http://www.choskim.me/how-to-install-mongodb-on-apples-mac-os-x/)

1. 다운 받은 파일 압축을 풀어서 그 내용물을 /usr/local/mongodb 폴더에 저장한다.

  <pre>
  $ cd /usr/local/mongodb/
  Onlydel-MacBook-Pro:mongodb onlydel$ ls -al
  total 152
  drwxr-xr-x   7 onlydel  wheel    238 Oct  2 14:26 .
  drwxr-xr-x  24 root     wheel    816 Oct  2 13:33 ..
  -rw-r--r--@  1 onlydel  wheel   8196 Oct  2 14:26 .DS_Store
  -rw-r--r--@  1 onlydel  wheel  34520 Aug 24 09:44 GNU-AGPL-3.0
  -rw-r--r--@  1 onlydel  wheel   1359 Aug 24 09:44 README
  -rw-r--r--@  1 onlydel  wheel  22660 Aug 24 09:44 THIRD-PARTY-NOTICES
  drwxr-xr-x@ 16 onlydel  wheel    544 Oct  2 13:30 bin
  </pre>

2. bash profile에 아래 처럼 mongodb path를 지정해 준다.

  <pre>
  $ nano ~/.bash_profile
  ...
  # 몽고디비
  export MONGO_PATH=/usr/local/mongodb
  export PATH=$PATH:$MONGO_PATH/bin
  ...</pre>


## 실행

실행파일 `mondod`를 실행하기 전에 아래 내용을 확인한다.

1. data를 저장할 data 디렉토리를 생성한다.
2. ~/Data/db에 생성하고 read/write가 가능하도록 권한을 부여한다.
3. data 디렉토리로 이동하고 mongod를 실행한다. 
4. `mondod`를 실행할때 data 디렉토리를 인자로 넘기지 않거나 data 디렉토리 안에서 실행하지 않으면 기본설정 디렉토리를 data 디렉토리로 사용하게 된다.(정확히는 모르겠지만 /data/db 인것 같은데)

<pre>
$ mkdir -p ~/data/db
$ cd ~/Data/db
$ mongod --dbpath ~/Data/db</pre>

위와 같이 실행하면 db 서버가 실행된다. 표현을 정확히 어떻게 해야할지 아직은 잘 모르겠지만 서버가 실행된다고 하자. 서버가 실행되면 연결을 기다리는 화면이 출력되고 클라언트의 접속을 기다린다.

<pre>
$ mongod --dbpath ~/Data/db
2015-10-02T13:43:34.536+0900 I JOURNAL  [initandlisten] journal dir=/Users/onlydel/Data/db/journal
2015-10-02T13:43:34.536+0900 I JOURNAL  [initandlisten] recover : no journal files present, no recovery needed
2015-10-02T13:43:34.550+0900 I JOURNAL  [durability] Durability thread started
2015-10-02T13:43:34.550+0900 I CONTROL  [initandlisten] MongoDB starting : pid=23183 port=27017 dbpath=/Users/onlydel/Data/db 64-bit host=Onlydel-MacBook-Pro.local
2015-10-02T13:43:34.550+0900 I JOURNAL  [journal writer] Journal writer thread started
2015-10-02T13:43:34.550+0900 I CONTROL  [initandlisten] db version v3.0.6
2015-10-02T13:43:34.550+0900 I CONTROL  [initandlisten] git version: 1ef45a23a4c5e3480ac919b28afcba3c615488f2
2015-10-02T13:43:34.550+0900 I CONTROL  [initandlisten] build info: Darwin mci-osx108-7.build.10gen.cc 12.5.0 Darwin Kernel Version 12.5.0: Sun Sep 29 13:33:47 PDT 2013; root:xnu-2050.48.12~1/RELEASE_X86_64 x86_64 BOOST_LIB_VERSION=1_49
2015-10-02T13:43:34.550+0900 I CONTROL  [initandlisten] allocator: system
2015-10-02T13:43:34.550+0900 I CONTROL  [initandlisten] options: { storage: { dbPath: "/Users/onlydel/Data/db" } }
2015-10-02T13:43:34.558+0900 I NETWORK  [initandlisten] waiting for connections on port 27017</pre>

## 연결

이제 db에 연결하기 위해 mongo shell을 이용해 접속해 본다. shell 프로그램은 `mongo`로 실행한다. 기본적으로 인자가 없으면 local의 27017포트로 접속을 시도한다. 실행하면 명령입력을 기다리는 프롬프트가 보인다.

<pre>
$ mongo
MongoDB shell version: 3.0.6
connecting to: test
Welcome to the MongoDB shell.
For interactive help, type "help".
For more comprehensive documentation, see
  http://docs.mongodb.org/
Questions? Try the support group
  http://groups.google.com/group/mongodb-user
>
</pre>

서버에 연결이되면 접속정보가 로그에 기록된다.

<pre>
...
2015-10-02T13:43:47.422+0900 I NETWORK  [initandlisten] connection accepted from 127.0.0.1:52672 #1 (1 connection now open)
...</pre>

## 연습

* shell에서 collection에 새로운 document를 하나 추가해 보자.

  <pre>
  &gt; db.mycoll.save({id:10, name:"cho"})
  WriteResult({ "nInserted" : 1 })</pre>

* 서버를 중지해 보자: 서버를 중지 하려면 shell에서 아래 코드처럼 admin 계정으로 접근한 다음 `db.shutdownServer()`로 중지하면 된다.
  
  <pre>
  $ mongo
  MongoDB shell version: 3.0.6
  connecting to: test
  > <mark>use admin</mark>
  switched to db admin
  > <mark>db.shutdownServer()</mark>
  2015-10-07T00:29:27.576+0900 I NETWORK  DBClientCursor::init call() failed
  server should be down...
  2015-10-07T00:29:27.579+0900 I NETWORK  trying reconnect to 127.0.0.1:27017 (127.0.0.1) failed
  2015-10-07T00:29:27.579+0900 W NETWORK  Failed to connect to 127.0.0.1:27017, reason: errno:61 Connection refused
  2015-10-07T00:29:27.579+0900 I NETWORK  reconnect 127.0.0.1:27017 (127.0.0.1) failed failed couldn't connect to server 127.0.0.1:27017 (127.0.0.1), connection attempt failed
  > exit
  bye
  </pre>

  또는 실행 콘솔이 열려 있다면 `CTRL+C`키로 바로 중지할 수도 있다.

## 관리툴

몽고디비 관리툴로 [robomongo](http://robomongo.org/)를 사용해 본다.
홈페이지에서 다운로드 받아 설치하고 실행 하면 연결정보가 뜬다. context menu에서 add하고 위에서 만든 기본 연결정보를 추가한다.

(localhost:27017, 사용자계정은 없음)으로 접속

## 참조

* [MongoDB](http://docs.mongodb.org/)
* [robomongo](http://robomongo.org/)
