---
layout: post
title: javascript에서 객체 정의
date:   2015-12-22 22:24:23 +9:00 GMT
categories: 
  - Javascript
tags: 
  - javascript
  - object
---

이 글은 javascript에서 객체를 정의하기 위해 자주 사용하는 방법에 대한 기록이다.

## 프로그래밍에서 객체는?
* 객체의 기본 개념은 알아서...
* 객체지향에 대한 공부도 각자 알아서...
* 이 글에서 중요한 내용은 객체가 상태(status), 행위(behavior)를 가지고 있다는 것.
* 상태란 속성(property) 또는 필드(field)로 구현될 수 있고, 행위는 메서드(method) 또는 함수(function)으로 구현 될 수 있다.

* 예를 들어 `사람`이란 객체
    - 이름(상태)
    - 나이(상태)
    - 말하기(행위)
    - ...

* 상속? 남자사람, 여자사람...

## javascript에서 객체를 만드는 기본틀
1. function을 이용하는 방법
    <pre class="prettyprint">
    var person = function() {..};</pre>

2. object 리터럴을 이용하는 방법
    <pre class="prettyprint">
    var preson = {..};</pre>

## 모던하면서 일반적인 방법은 다 function을 사용한다.


### 1. method를 내장 하는 방법

<pre class="prettyprint">
var Person = function(name, age) {

  this.name = name;
  this.age = age;

  var _speaked = false;

  this.speak = function(msg) {
    console.log(msg);
    _speaked = true;
  }

  this.hasBeenSpeaked = function() {
    return _speaked;
  }
}

//사용
var person = new Person('조원홍', 27);
if (!person.hasBeenSpeaked) {
    person.speak('소리질러');
}
</pre>

* 모든 속성과 메서드를 하나의 function안에 한꺼번에 정의 한다.
* var로 정의 한 변수는 private member처럼 쓸 수 있다.
* this로 정의한 변수는 public member처럼 쓸 수 있다.
* 문제는 인스턴스가 생성될때 마다 모든 member들이 재생성 된다. 이건 완전 비효율이지.

### 2. prototype사용

<pre class="prettyprint">
var Person = function(name, age) {
  this.name = name;
  this.age = age;
  this.speaked = false;

  //scope이 다르기 때문에 prototype에 정의된 메서드에서 사용불가
  var _speaked = false;
}

Person.prototype.speak = function(msg) {
    console.log(msg);
    speaked = true;
}

Person.prototype.hasBeenSpeaked = function() {
    return this.speaked;
}

//사용
var person = new Person('조원홍', 27);
if (person.hasBeenSpeaked() === false) {
    person.speak('소리질러');
}

//상속은?
var Woman = function() {
}

Woman.prototype = new Person();

</pre>

* 정의된 객체에 prototype을 이용해 속성이나 메서드를 추가할 수 있다.
* 상속이라기 보다는 상속 비스무리한것? 어쨋거나 프로토타입체인을 이용해서 상속의 효과를 얻을 수 있다.

### 3. module pattern

<pre class="prettyprint">
var Person = function(name, age) {

  var _speaked = false;

  var privateMethod = function() {
  }

  return {
    name: name,
    age: age,
    speak: function(msg) {
      console.log(msg);
      _speaked = true;
    },
    hasBeenSpeaked: function() {
      return _speaked;
    }
  }
}

//사용
var person = Person('조원홍', 27);
if (person.hasBeenSpeaked() === false) {
    person.speak('소리질러');
}</pre>

* 객체를 반환할 경우 `new`키워드 생략 가능
* prototype속성은 아무런 영향을 미치지 못한다.
* 상속이 어렵다. 상속하려면 모든 메소드를 각각 복제해야 한다.
* 내장 패턴과 마찬가지로 메모리를 좀더 사용한다.

### 참고의 참고로 es6에서 class

<pre class="pretryprint">
import OtherModule from 'other-module';

class Person {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }

    speak(message) {
        console.log(message);
    }
}

export default Person;
</pre>

* 상속도 좀더 편하게

<pre class="pretryprint">
import Person from './persion'; // persion.js

export default class Woman extends Persion {
    constructor(name, age) {
        super(name, age);
    }

    speak(message) {
        super.speak(message);
        console.log('Woman message: ' + message)
    }
}
</pre>

* hoisting문제가 있다.
* 보통은 서버모듈을 구성하거나 babel, webpack같은 빌드툴을 이용한 라이브러리 개발시 좋다.
* 앞으로는 이런 방향이 일반화 될것. 2,3년?
 


---
**참조**

* [javascript garden](http://bonsaiden.github.io/JavaScript-Garden/ko/){:target="_blank"}
* [javascript design pattern](http://addyosmani.com/resources/essentialjsdesignpatterns/book/)