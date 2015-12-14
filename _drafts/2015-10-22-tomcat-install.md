---
layout: post
title: Tomcat 설치하기
date:   2015-10-21 13:24:23 +9:00 GMT
categories: 
  - Another Code
tags: 
  - html
  - jquery
  - parseHTML
  - iframe
---

## 설치
* Download
<pre>

Onlydel-MacBook-Pro:Tomcat onlydel$ sudo chown -R onlydel /Library/Tomcat
Onlydel-MacBook-Pro:Tomcat onlydel$ sudo chmod +x /Library/Tomcat/bin/*.sh

<mark>Onlydel-MacBook-Pro:Tomcat onlydel$ /Library/Tomcat/bin/startup.sh</mark>
Using CATALINA_BASE:   /Library/Tomcat
Using CATALINA_HOME:   /Library/Tomcat
Using CATALINA_TMPDIR: /Library/Tomcat/temp
Using JRE_HOME:        /Library/Java/JavaVirtualMachines/jdk1.8.0_60.jdk/Contents/Home
Using CLASSPATH:       /Library/Tomcat/bin/bootstrap.jar:/Library/Tomcat/bin/tomcat-juli.jar
Tomcat started.

<mark>Onlydel-MacBook-Pro:Tomcat onlydel$ /Library/Tomcat/bin/shutdown.sh</mark>
Using CATALINA_BASE:   /Library/Tomcat
Using CATALINA_HOME:   /Library/Tomcat
Using CATALINA_TMPDIR: /Library/Tomcat/temp
Using JRE_HOME:        /Library/Java/JavaVirtualMachines/jdk1.8.0_60.jdk/Contents/Home
Using CLASSPATH:       /Library/Tomcat/bin/bootstrap.jar:/Library/Tomcat/bin/tomcat-juli.jar
Onlydel-MacBook-Pro:Tomcat onlydel$</pre>

http://localshot:8080 접속




---
**참조**

* [https://wolfpaulus.com/journal/mac/tomcat8/](https://wolfpaulus.com/journal/mac/tomcat8/){:target="_blank"}

