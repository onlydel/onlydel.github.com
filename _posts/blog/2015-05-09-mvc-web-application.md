---
layout: post
title: MVC Web Application에서 재사용 가능한 Authentication라이브러리 만들기
date:   2015-05-09 21:13:31 +9:00 GMT
categories:
  - ASP.NET
  - draft
tags: 
  - MVC
  - Authentication
  - Identity
---

### 기술
* ASP.NET 4.5
* MVC 5
* EntityFramework 6.1.3
* ASP.NET Identity 2.1.0
* Microsoft.Owin 3.0.1
* Owin 1.0
* Visual Studio Community 2013

### 목적
ASP.NET MVC Web Application(MVC앱)개발시 인증 처리를 위한 재사용 가능한 라이브러리를 만드는 방법을 정리해 보겠습니다. Visual Studio(VS)에서 새로운 MVC앱 프로젝트를 생성하면서 Individual User Authentication 옵션을 선택하면 완전한 사용자 인증관리 모듈을 구현해 줍니다. 이 모듈을 라이브러리로 분리하는 방법으로 작업해 보겠습니다.

### 구조
사용자 인증 모듈 라이브러리는 Model과 Controller부분을 각각 다른 라이브러리 프로젝트로 만들고 MVC Web Application에 Login페이지와 같은 View영역을 작성하겠습니다. 필요에 따라 다양한 방법으로 구조를 바꾸어 구현이 가능 하겠지만, Web API Application의 Token인증 방식에서도 사용할 수 있도록 Model과 Controller를 별도의 라이브러리로 구성해 보겠습니다.