---
layout: post
title: javascript tutorial
date:   2015-11-05 13:24:23 +9:00 GMT
categories: 
  - Another Code
tags: 
  - html
---

[http://www.w3schools.com/html/html_intro.asp](http://www.w3schools.com/js/js_intro.asp) 사이트 부터 시작
  
## JavaScript Introduction

## 자바스크립트 소개

---

JavaScript is the most popular programming language in the world.    
This page contains some examples of what JavaScript can do.

자바스크립트는 세계에서 최고로 인기있는 프로그래밍 언어이다.  
이 페이지에는 자바스크립트가 어떤동작을 하는지에대한 약간의 예제가 들어가 있습니다.

---

### JavaScript Can Change HTML Content  

### 자바스크립트는 HTML내용을 변화 시킬 수 있습니다.

One of many HTML methods is getElementById().  
This example uses the method to "find" an HTML element (with id="demo"), and changes the element content (innerHTML) to "Hello JavaScript":

 getElementById()는 많은 HTML 방법중에 하나입니다.  
이 예시는 HTML요소에서(with id="demo")를 찾아서, (innerHTML)요소안을 "Hello JavaScript"로 변화시키는 방법입니다.

### Example

### 예

<pre class="prettyprint">
document.getElementById("demo").innerHTML = "Hello JavaScript";
</pre>

---

### JavaScript Can Change HTML Attributes

### HTML 속성은 자바스크립트에 의해서 변환이 가능합니다

This example changes an HTML image, by changing the src attribute of an <img> tag:

이 예시는 HTML 이미지를 이미지 태그의 src속성에 의해서 바뀝니다.

![](http://www.w3schools.com/js/pic_bulboff.gif)

---

### JavaScript Can Change HTML Styles (CSS)

### 자바스크립트는 HTML (CSS)스타일을 바꿀 수 있습니다.

Changing the style of an HTML element, is a variant of changing an HTML attribute:

HTML요소에서 스타일을 변경한 HTML의 결과이다:

### Example

<pre class="prettyprint">
document.getElementById("demo").style.fontSize = "25px";
</pre>

---

### JavaScript Can Validate Data

### 자바스크립트는 데이터 인증이 가능합니다.

JavaScript is often used to validate input:  
Please input a number between 1 and 10  
 <input type="text"><input type="button" value="Submit">
  
자바스크립트는 흔이 입력을 인증하는데 사용합니다.  
1부터10사이에 숫자를 넣어보세요.

---

## Did You Know?

## 당신은 알고 있나요?

JavaScript and Java are completely different languages, both in concept and design.  
JavaScript was invented by Brendan Eich in 1995, and became an ECMA standard in 1997.  
ECMA-262 is the official name. ECMAScript 6 (released in June 2015) is the latest official version of JavaScript.

자바스크립트와 자바는 둘다 언어뿐만아니라 개념이나 만드는 방법도 다릅니다.  
자바스크립트는 1995년에 Brendan Eich라는 인물에의해 발명되었고, 1997년 ECMA표준이되었다.
ECMA-262는 공식적으로 알려진 이름이다. ECMASctipt6(2015년 6월에 출시)은 자바스크립트의 공식적인 최신 버전입니다.

---