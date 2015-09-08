---
layout: post
title: AngulaJS 연습
date:   2015-09-02 15:30:31 +9:00 GMT
categories: 
  - Javascript
tags: 
  - AngularJS
---

## AngularJS Tutorial

#### 왜 AngularJS를 써야 하나요?

* 좀더 쉽게 JavaScript코드를 구조화 할 수 있다. (웹 페이지에서 JavaScript코드가 복잡해지기 시작하면 맨붕오는거 알죠?)
* 반응형 웹사이트 만드는데 도움됩니다.
* JQuery랑 아주 잘 어울립니다.
* 테스트하기 쉽습니다.

#### AngularJS가 뭔가요?

클라이언트 사이트 웹 애플리케이션 개발할때 HTML과 상호작용할 수 있는 프레임워크

#### 지시자(Directives)

<pre class="prettyprint">
&lt;html <mark>ng-app</mark>="myApp"&gt;
    &lt;div <mark>ng-controller</mark>="myController"&gt;&lt;/div&gt;
&lt;/html&gt;
</pre>

#### 모듈(Modules)

<pre class="prettyprint">
&lt;html ng-app=&quot;myApp&quot;&gt;
&lt;/html&gt;
</pre>

<pre class="prettyprint">
var app = angular.module("myApp", []);
</pre>

#### 익스프레션(Expressions)

<pre class="prettyprint">
{% raw %}{{}}{% endraw %}
</pre>

#### 컨트롤러(Controllers)


#### 필터(Filters)
angular에서 필터를 데이터를 출력하기 위한 방법으로 사용되며 아래 코드 처럼 정의 할 수 있습니다.

<pre class="prettyprint">
{% raw %}{{ data | filter:options }}

//date
{{ '1388123412313' | date:'MM/dd/yyyy @ h:mma' }} 12/27/1013 @ 12:50AM

{% endraw %}
</pre>

필터에 사용되는 파이프라인("|")은 "다음과 같이 내보내기 해라!"라는 의미로 해석될 수 있습니다.

#### ng-show / ng-hide

#### ng-click

#### ng-class

#### ng-model 지시자

#### 폼 컨트롤하기

#### 폼 벨리데이션

#### Custom Directives



---
**참조**

* [w3School AngularJS Tutorial](http://www.w3schools.com/angular/){:target="_blank"}
* [Code School AngularJS](http://campus.codeschool.com/courses/shaping-up-with-angular-js/intro){:target="_blank"}
* [Doc Api Reference](https://docs.angularjs.org/api){:target="_blank"}
* [AngrularJS testing framework : Protractor](https://github.com/angular/protractor){:target="_blank"}