---
layout: post
title: javascript tutorial
date:   2015-11-05 13:24:23 +9:00 GMT
categories: 
  - Another Code
tags: 
  - JavaScript
---

[http://www.w3schools.com/html/html_intro.asp](http://www.w3schools.com/js/js_intro.asp) 사이트 부터 시작
  
# JavaScript Introduction

# 자바스크립트 소개

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

[링크](http://www.w3schools.com/js/tryit.asp?filename=tryjs_intro_lightbulb)

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
[링크](http://www.w3schools.com/js/tryit.asp?filename=tryjs_intro_validate)

---

### Did You Know?

### 당신은 알고 있나요?

JavaScript and Java are completely different languages, both in concept and design.  
JavaScript was invented by Brendan Eich in 1995, and became an ECMA standard in 1997.  
ECMA-262 is the official name. ECMAScript 6 (released in June 2015) is the latest official version of JavaScript.

자바스크립트와 자바는 둘다 언어뿐만아니라 개념이나 만드는 방법도 다릅니다.  
자바스크립트는 1995년에 Brendan Eich라는 인물에의해 발명되었고, 1997년 ECMA표준이되었다.
ECMA-262는 공식적으로 알려진 이름이다. ECMASctipt6(2015년 6월에 출시)은 자바스크립트의 공식적인 최신 버전입니다.

---

# JavaScript Where To

# 자바스크립트는 어디에

JavaScript can be placed in the <body> and the <head> sections of an HTML page.
 
자바스크립트는 HTML페이지의 <body>나<head>부분에 배치될 수 있습니다.

<pre class="prettyprint">
The &lt;script&gt; Tag
In HTML, JavaScript code must be inserted between &lt;script&gt; and &lt;/script&gt; tags.

스크립트 태그  
HTML안에서는, 자바스크립트 코드를 &lt;script&gt;와&lt;/script&gt;사이에 끼워넣어야 합니다.

Example  예
&lt;script&gt;
document.getElementById("demo").innerHTML = "My First JavaScript";
&lt;/script&gt;

Older examples may use a type attribute: &lt;script type="text/javascript"&gt;.
The type attribute is not required. JavaScript is the default scripting language in HTML.

다른 예로는 이런식으로 바꾸어 사용할 수도 있습니다:&lt;script type="text/javascript"&gt;.
그 방식은 속성이 필요하지 않습니다. 자바스크립트는 HTML의 기본 스크립트 언어입니다.

</pre>
---

### JavaScript Functions and Events

### 자바스크립트의 함수와 이벤트

A JavaScript function is a block of JavaScript code, that can be executed when "asked" for.   
For example, a function can be executed when an event occurs, like when the user clicks a button.   
You will learn much more about functions and events in later chapters.

자바스크립트의 함수에 대한 "요구"가 실행될 수 있는 자바스크립트의 코드 블록입니다.
예를들어, 어떤 함수의 이벤트의 실행이나, 어떤 사용자의 버튼이 눌리는 것과 비슷합니다.
당신은 더많은 함수와 이벤트에 대해서 이장의 뒤에서 배울것 입니다.

---

### JavaScript in <head> or <body>

### 자바스크립트의 <head>와<body>안에

You can place any number of scripts in an HTML document.   
Scripts can be placed in the <body>, or in the <head> section of an HTML page, or in both.   
Keeping all code in one place, is always a good habit.

당신은 많은 수의 스크립트를 HTML문서에 배치할 수 있습니다.
스크립트는 <body>안이나, 또는 HTML페이지의 <head>부분이나, 또는 둘다 가능합니다. 
한 곳에서 항상 모든 코드를 저장하는 것이 좋은 습관입니다.

---

### JavaScript in <head>   

### 자바스크립트<head>안에

In this example, a JavaScript function is placed in the <head> section of an HTML page.   
The function is invoked (called) when a button is clicked:

이것을 예로들자면, 자바스크립트 함수는 HTML페이지의 <head>부분 안에 배치됩니다.
버튼이 클릭될 때 이 함수를 호출합니다:

Example 예

<pre class="prettyprint">
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
&lt;script&gt;
function myFunction() {
    document.getElementById("demo").innerHTML = "Paragraph changed.";
}
&lt;/script&gt;
&lt;/head&gt;

&lt;body&gt;

&lt;h1&gt;My Web Page&lt;/h1&gt;

&lt;p id="demo"&gt;A Paragraph&lt;/p&gt;

&lt;button type="button" onclick="myFunction()">Try it&lt;/button&gt;

&lt;/body&gt;
&lt;/html&gt;
</pre>

---

### JavaScript in <body>

### 자바스크립트<body>안에

In this example, a JavaScript function is placed in the <body> section of an HTML page.
The function is invoked (called) when a button is clicked:

이것을 예로들자면, 자바스크립트 함수는 HTML페이지의 <body>부분 안에 배치됩니다.
버튼이 클릭될 때 함수가 호출됩니다:

Example 예
<pre class="prettyprint">
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;body&gt;

&lt;h1&gt;My Web Page&lt;/h1&gt;

&lt;p id="demo"&gt;A Paragraph&lt;/p&gt;

&lt;button type="button" onclick="myFunction()"&gt;Try it&lt;/button&gt;

&lt;script&gt;
function myFunction() {
   document.getElementById("demo").innerHTML = "Paragraph changed.";
}
&lt;/script&gt;

&lt;/body&gt;
&lt;/html&gt;
</pre>

It is a good idea to place scripts at the bottom of the body element.   
This can improve page load, because HTML display is not blocked by scripts loading.
 
body요소 아래다 스크립트 장소를 지정하는 것이 좋습니다.
이것은 페이지의 로드를 차단하기 때문에 HTML화면에 스크립트 로딩이 앞에서 차단되기 않기 위해서 입니다.


---

### External JavaScript

### 외부 자바스크립트

<pre class="prettyprint">
Scripts can also be placed in external files.   
External scripts are practical when the same code is used in many different web pages.   
JavaScript files have the file extension .js.  
To use an external script, put the name of the script file in the src (source) attribute of the &lt;script&gt; tag:

스크립트는 외부 파일에 배치 될 수도 있습니다.
코드가 같고 다양한 웹 페이지에서는 외부 스크립트를 사용하는 것이 실용적 입니다.
자바스크립트 파일의 파일확장자명은.js입니다.
&lt;script&gt;태그의 SRC(소스) 속성에 스크립트 파일을 넣어서 외부 스크립트를 사용합니다.:

</pre>

Example 예
<pre class="prettyprint">
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;body&gt;
&lt;script src="myScript.js"&gt;&lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>

<pre class="prettyprint">
You can place an external script reference in &lt;head&gt; or &lt;body&gt; as you like.  
The script will behave as if it was located exactly where the &lt;script&gt; tag is located.
External scripts cannot contain &lt;script&gt; tags.

당신은 &lt;head&gt;와&lt;body&gt;안에 당신이 좋아하는 장소에 외부 스크립트를 배치할 수 있습니다.
이 &lt;script&gt;태그에 위치한 것처럼 스크립트가 동작합니다.
...외부 스크립트들은 &lt;script&gt;태그들 속에 할 수 없습니다.
</pre>

---

### External JavaScript Advantages

### 외부 자바스크립트의 이로운점

Placing JavaScripts in external files has some advantages:

외부 파일은 자바스크립트에 이로운점이 약간 있습니다.

*  It separates HTML and code
*  It makes HTML and JavaScript easier to read and maintain
*  Cached JavaScript files can speed up page loads

*  HTML과 코드를 따로 입니다.
*  HTML과 자바스크립트로 만들면 쉽게 읽고 유지 할 수 있습니다.
*  저장된 자바스크립트 파일은 페이지 로드 속도를 올릴 수 있습니다.

---

# JavaScript Output

# 자바스크립트 출력

JavaScript does NOT have any built-in print or display functions.

자바스크립트는 자체에서 보여주는 것과 화면에 보여주는 함수가 존재하지 않습니다.

### JavaScript Display Possibilities

### 자바스크립트는 보여주는것이 가능합니다.

JavaScript can "display" data in different ways:

자바스크립트는 보여주는 방식에 차이가 있습니다:

*  Writing into an alert box, using window.alert().
*  Writing into the HTML output using document.write().
*  Writing into an HTML element, using innerHTML.
*  Writing into the browser console, using console.log().

*  경고 상자 안에다가 글을 쓸때는 window.alert().를 사용합니다.
*  HTML안에다 출력할 글을 쓸때는 document.write()를 사용합니다.
*  HTML요소 안에다 글을쓸때는 innerHTML을 사용합니다.
*  브라우저 콘솔안에다 글을 쓸때는 console.log()를 사용합니다.

---

### Using window.alert()

### window.alert() 사용

You can use an alert box to display data:

당신은 경고상자에 데이터가 보여지게 할 수 있습니다.

Example 예
<pre class="prettyprint">
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;body&gt;

&lt;h1&gt;My First Web Page&lt;/h1&gt;
&lt;p&gt;My first paragraph.&lt;/p&gt;

&lt;script&gt;
window.alert(5 + 6);
&lt;/script&gt;

&lt;/body&gt;
&lt;/html&gt;
</pre>

---

### Using document.write()

### document.write()사용

For testing purposes, it is convenient to use document.write():

편리하게 사용하기 위해 document.write()를 다음과 같이 사용하여 테스트 해보겠습니다.:

Example
<pre class="prettyprint">
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;body&gt;

&lt;h1&gt;My First Web Page&lt;/h1&gt;
&lt;p&gt;My first paragraph.&lt;/p&gt;

&lt;script&gt;
window.write(5 + 6);
&lt;/script&gt;

&lt;/body&gt;
&lt;/html&gt;
</pre>
Using document.write() after an HTML document is fully loaded, will delete all existing HTML:  
HTML문서가 완전히 로드 된 후에 document.write()를 사용합니다. 기존에 사용하던 HTML을 삭제합니다:
<pre class="prettyprint">
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;body&gt;

&lt;h1&gt;My First Web Page&lt;/h1&gt;
&lt;p&gt;My first paragraph.&lt;/p&gt;

&lt;button onclick="document.write(5 + 6)"&gt;Try it&lt;/button&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>
The document.write() method should be used only for testing.

document.write() 방법은 테스트용으로만 사용 되어야 합니다.

---

### Using innerHTML

### innerHTML사용

To access an HTML element, JavaScript can use the document.getElementById(id) method.  
The id attribute defines the HTML element. The innerHTML property defines the HTML content:

HTML요소에 들어가려면, 자바스크립트의 document.getElimentById(id)방법을 사용해야 합니다.  
그 아이디속성은 HTML의 요소를 정의합니다. innerHTML속성 정의는 HTML내용의 입니다.

<pre class="prettyprint">
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;body&gt;

&lt;h1&gt;My First Web Page&lt;/h1&gt;
&lt;p&gt;My first paragraph.&lt;/p&gt;

&lt;p id="demo"&gt;&lt;/p&gt;

&lt;script&gt;
documnet.getElementById("demo").innerHTML = 5 + 6;
&lt;/script&gt;

&lt;/body&gt;
&lt;/html&gt;
</pre>
To "display data" in HTML, (in most cases) you will set the value of an innerHTML property.
 
(대부분의 경우)HTML로"데이터 표시"를 위해, 당신은 innerHTML속성의 값을 설정 해야합니다.

---

### Using console.log()

### console.log()사용

In your browser, you can use the console.log() method to display data.  
Activate the browser console with F12, and select "Console" in the menu.

당신의 브라우저안에서, console.log()방법을 사용해서 데이터를 보여줄 수 있습니다.  
F12로 브라우저의 콘솔을 활성화 시키고, 메뉴에서 콘솔을 선택합니다.

Example
<pre class="prettyprint">
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;body&gt;

&lt;h1&gt;My First Web Page&lt;/h1&gt;
&lt;p&gt;My first paragraph.&lt;/p&gt;

&lt;p id="demo"&gt;&lt;/p&gt;

&lt;script&gt;
console.log(5 + 6);
&lt;/script&gt;

&lt;/body&gt;
&lt;/html&gt;
</pre>

---

# JavaScript Syntax 

# 자바스크립트 문법

JavaScript syntax is the set of rules, how JavaScript programs are constructed.

자바스크립트 문법은, 어떻게 자바스크립트 프로그램이 만들어지는가에 대한 규칙이다.

### JavaScript Programs

### 자바스크립트 프로그램

A computer program is a list of "instructions" to be "executed" by the computer.   
In a programming language, these program instructions are called statements.   
JavaScript is a programming language.   
JavaScript statements are separated by semicolons.  

컴퓨터에서의 목록중에 '지시'로 '실행'되는것이 컴퓨터 프로그램입니다.  
프로그램 언어 안에서는 프로그램 명령들을 문 이라고 불린다.  
자바스크립트는 프로그래밍 언어입니다.  
자바스크립트 문은 세미콜론으로 구분됩니다.

Example
<pre class="prettyprint">
var x = 5;
var y = 6;
var z = x + y;
</pre>
In HTML, JavaScript programs can be executed by the web browser.  
HTML안에서의, 자바스크립트 프로그램은 웹 브라우저에서 실행이 가능 합니다.

---

### JavaScript Statements

### 자바스크립트 문

JavaScript statements are composed of:  
Values, Operators, Expressions, Keywords, and Comments.

자바스크립트 문의 구성:
Values, Operators, Expressions, Keywords, and Comments.  

---

### JavaScript Values

### 자바스크립트 values

The JavaScript syntax defines two types of values: Fixed values and variable values.  
Fixed values are called literals. Variable values are called variables.

자바스크립트 문법의 값의 두가지 유형으로는 : 고정된 값과 변경되는 값 입니다.  
고정된 값은 리터럴(상수) 이라고 불린다. 변하는 값은 변수라고 한다.

---

### JavaScript Literals

### 자바스크립트 리터럴

The most important rules for writing fixed values are:   
Numbers are written with or without decimals:

고정된 값을 쓸때 가장 중요한 점은:  
숫자를 소수점이 없이 쓰거나 같이 쓰일경우: 
<pre class="prettyprint">
10.50

1001
</pre>
Strings are text, written within double or single quotes:  
문자열에 글씨는, 따옴표1개 또는 2개안에 쓰입니다:
<pre class="prettyprint">
"John Doe"

'John Doe'
</pre>

---

### JavaScript Variables

### 자바스크립트 변수

In a programming language, variables are used to store data values.  
JavaScript uses the var keyword to define variables.  
An equal sign is used to assign values to variables.  
In this example, x is defined as a variable. Then, x is assigned (given) the value 6:

프로그래밍 언어에서 변수는 데이터 값을 저장하는데 사용합니다.  
자바스크립트에서는 변수의 핵심단어를 var로 정의하여 사용합니다.
=은 변수에 값을 할당하는데 사용합니다.  
예제에서는 x는 변수로 정의 합니다. 그x에 6이라는 값으로 부여합니다.
<pre class="prettyprint">
var x;

x = 6;
</pre>

### JavaScript Operators

### 자바스크립트 연산

JavaScript uses an assignment operator ( = ) to assign values to variables:  
자바스크립트 대입연산자(=)를 사용해서 변수에 값을 부여합니다:
<pre class="prettyprint">
var x = 5;
var y = 6;
</pre>
JavaScript uses arithmetic operators ( + - *  / ) to compute values:  
자바스크립트의 산수연산자로는(+ - * /)로 값을 계산합니다: 
<pre class="prettyprint">
(5 + 6) * 10
</pre>

### JavaScript Expressions

### 자바스크립트 표현

An expression is a combination of values, variables, and operators, which computes to a value.  
The computation is called an evaluation.   
For example, 5 * 10 evaluates to 50:

expression은 값, 변수, 연산자들의 어떤 값에 대한 결과물입니다.  
그것은 계산은 값이라고 불립니다.  
예를들어 5*10의 결과는 50입니다:  
<pre class="prettyprint">
5 * 10
</pre>
Expressions can also contain variable values:  
게다가 Expressions는 변수에 들어있는 값도 가능합니다:  
<pre class="prettyprint">
x * 10
</pre>
The values can be of various types, such as numbers and strings.   
For example, "John" + " " + "Doe", evaluates to "John Doe":

이미 앞에 언급한 문자나 숫자도 다양한 종류의 값으로 가능합니다.  
예를들어, "John" + " " + "Doe"은 "John Doe"로 평가 됩니다:
<pre class="prettyprint">
"John" + " " + "Doe"
</pre>

### JavaScript Keywords

### 자바스크립트 키워드

JavaScript keywords are used to identify actions to be performed.   
The var keyword tells the browser to create a new variable:

자바스크립트 키워드는 행동을 확인할때 사용합니다.  
var키워드는 브라우저에서 새로운 변수를 만드는것을 말합니다.  
<pre class="prettyprint">
var x = 5 + 6;
var y = x * 10;
</pre>

---

### JavaScript Comments

### 자바스크립트 주석

Not all JavaScript statements are "executed".   
Code after double slashes // or between /* and */ is treated as a comment.   
Comments are ignored, and will not be executed: 

모든 자바스크립트는 "실행"되는것이 아닙니다.
주석은 2개의 슬레쉬// 다음에 아니면 /*와*/ 사이에 코드의 내용을 취급합니다.
주석은 무시됩니다, 그리고 실행되지 않습니다.
<pre class="prettyprint">
var x = 5;   // I will be executed

// var x = 6;   I will NOT be executed
</pre>

---

### JavaScript Identifiers

### 자바스크립트 식별자

Identifiers are names.   
In JavaScript, identifiers are used to name variables (and keywords, and functions, and labels).   
The rules for legal names are much the same in most programming languages.   
In JavaScript, the first character must be a letter, an underscore (_), or a dollar sign ($).   
Subsequent characters may be letters, digits, underscores, or dollar signs.   
Numbers are not allowed as the first character.  
This way JavaScript can easily distinguish identifiers from numbers.

식별자의 이름들입니다.
자바스크립트안에는, 변수에 식별자의 이름을 사용합니다(키워드나 함수나 라벨).   
법적인 이름에대한 규칙은 대부분의 프로그래밍 언어들이 같다.  
식별자를 구성하는 첫번째 글자는 반드시'문자'나'밑줄_'이나 '달러$'로 시작되어야 합니다. 
첫글자 다음 문자로는 '문자' '숫자' '밑줄_' 또는 '달러$' 표시를 할 수 있습니다.  
숫자는 문자의 첫번째로 오는것은 허용하지 않습니다.  
자바스크립트는 숫자로 식별자를 쉽게 구별할 수 있습니다.  

---

### JavaScript is Case Sensitive

### 자바스크립트 대소문자를 구별합니다.

All JavaScript identifiers are case sensitive.    
The variables lastName and lastname, are two different variables.

모든 자바스크립트 식별자는 대소문자를 구별합니다.
변수lastName과lastname 2개는 다른 변수 입니다.
<pre class="prettyprint">
lastName = "Doe";
lastname = "Peterson";
</pre>
JavaScript does not interpret VAR or Var as the keyword var.  
자바스크립트는 VAR또는Var로 해석하지 않고 키워드는 var 입니다.

---

### JavaScript and Camel Case

### 자바스크립트 와 낙타대문자

Historically, programmers have used three ways of joining multiple words into one variable name:  
Hyphens:  
first-name, last-name, master-card, inter-city.  
Underscore:  
first_name, last_name, master_card, inter_city.  
Camel Case:  
FirstName, LastName, MasterCard, InterCity.

역사적으로, 프로그래머들은 하나의 변수이름에 여러가지 단어를 결합하는 방법으로 세 가지 방법이 있습니다:  
하이픈: -  first-name, last-name, master-card, inter-city.  
밑줄: _  first_name, last_name, master_card, inter_city.  
낙타대문자: FirstName, LastName, MasterCard, InterCity.

![](http://www.w3schools.com/js/pic_camelcase.jpg)

In programming languages, especially in JavaScript, camel case often starts with a lowercase letter:  
firstName, lastName, masterCard, interCity.  
Hyphens are not allowed in JavaScript. It is reserved for subtractions. 

자바스크립트 프로그래밍 언어에서는 종종 낙타대문자의 시작이 소문자로 시작하는 경우도 종종있다.  
firstName, lastName, masterCard, interCity.  
하이픈은 자바스크립트에서 사용할수 없습니다. 그것은 빼기로 예약하였습니다.

---

### JavaScript Character Set

### 자바스크립트 문자 세트

JavaScript uses the Unicode character set.  
Unicode covers (almost) all the characters, punctuations, and symbols in the world.  
For a closer look, please study our Complete Unicode Reference.

자바스크립트는 유니코드 문자 세트를 사용합니다.  
유니코드는 (거의)세상의 모든 문자,문장 부호 및 기호를 포함 합니다.  
끝내기전에 잠깐 들여다 보실려면, 유니코드에 대해서 부가적으로 공부하시려면 여기에 있습니다.

---
