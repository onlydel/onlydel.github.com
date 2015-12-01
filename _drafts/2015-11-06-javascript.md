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

<pre class="prettyprint">
Example
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



<pre class="prettyprint">
Example
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

&lt;script&gt;
Example
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

<pre class="prettyprint">
Example
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

<pre class="prettyprint">
Example
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

<pre class="prettyprint">
Example
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

<pre class="prettyprint">
Example
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

<pre class="prettyprint">
Example
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;body&gt;

&lt;h1&gt;My First Web Page&lt;/h1&gt;
&lt;p&gt;My first paragraph.&lt;/p&gt;

&lt;script&gt;
document.write(5 + 6);
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

HTML요소에 들어가려면, 자바스크립트의 document.getElementById(id)방법을 사용해야 합니다.  
그 아이디속성은 HTML의 요소를 정의합니다. innerHTML속성 정의는 HTML내용의 입니다.

<pre class="prettyprint">
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;body&gt;

&lt;h1&gt;My First Web Page&lt;/h1&gt;
&lt;p&gt;My first paragraph.&lt;/p&gt;

&lt;p id="demo"&gt;&lt;/p&gt;

&lt;script&gt;
document.getElementById("demo").innerHTML = 5 + 6;
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

<pre class="prettyprint">
Example
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

<pre class="prettyprint">
Example
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
숫자를 소수점이 없이 쓰일경우: 

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

### 자바스크립트 연산자

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
그것의 계산은 evaluation라고 불립니다.   
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

모든 자바스크립트가 전부 "실행"되는 것은 아닙니다.  
주석은 2개의 슬레쉬// 다음에 아니면 /* 와 */ 사이에 코드의 내용을 취급합니다. 
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
자바스크립트에서는, 변수에 식별자의 이름을 사용합니다(키워드나 함수나 라벨).   
합법적인 이름에대한 규칙은 대부분의 프로그밍 언어들에서 같습니다.   
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
For a closer look, please study our [Complete Unicode Reference](http://www.w3schools.com/charsets/ref_html_utf8.asp).

자바스크립트는 유니코드 문자 세트를 사용합니다.  
유니코드는 (거의)세상의 모든 문자,문장 부호 및 기호를 포함 합니다.  
끝내기전에 잠깐 들여다 보실려면, 유니코드에 대해서 부가적으로 공부하시려면 여기에 있습니다.

---

---

# JavaScript Statements

# 자바스크립트 문 

---

In HTML, JavaScript statements are "instructions" to be "executed" by the web browser.

HTML안에는 자바스크립트 문은 웹브라우저의 지시와 지침 입니다.

---

### JavaScript Statements

### 자바스크립트 문

This statement tells the browser to write "Hello Dolly." inside an HTML element with id="demo":

이 문장은 브라우저에 Hello Dolly를 쓸수있는 것을 말합니다. HTML 요소 안에 id를 demo로 함께 사용합니다.

<pre class="prettyprint">
Example
document.getElementById("demo").innerHTML = "Hello Dolly.";
</pre>

---

### JavaScript Programs

### 자바스크립트 프로그램

Most JavaScript programs contain many JavaScript statements.   
The statements are executed, one by one, in the same order as they are written.   
In this example, x, y, and z is given values, and finally z is displayed:

최고의 자바스크립트 프로그램은 많은 자바스크립트 문이 들어 있습니다.  
그 문은 입력한 순서와 동일한 순서로 하나하나씩 순차적으로 실행 됩니다.
이 예제는 x, y에 값을 주고 마지막으로 z에 표시합니다:

<pre class="prettyprint">
Example
var x = 5;
var y = 6;
var z = x + y;
document.getElementById("demo").innerHTML = z;
</pre>

JavaScript programs (and JavaScript statements) are often called JavaScript code.  
자바스크립트 프로그램은 흔히 자바스크립트 코드라고도 불립니다.

---

### Semicolons ;

### 세미콜론;

Semicolons separate JavaScript statements.   
Add a semicolon at the end of each executable statement:

세미콜론은 자바스크립트 문을 분리합니다.  
각 실행 문장 끝에 세미콜론을 추가합니다.:

<pre class="prettyprint">
a = 5;
b = 6;
c = a + b;
</pre>

When separated by semicolons, multiple statements on one line are allowed:  
세미콜론으로 많은 문장을 한줄로 구역을 나누어 사용할 수 있습니다.:

<pre class="prettyprint">
a = 5; b = 6; c = a + b;
</pre>

On the web, you might see examples without semicolons.  
Ending statements with semicolon is not required, but highly recommended.

웹에는 당신의 세미콜론이 없는 예가 보일 것 입니다.   
끝에 세미콜론을 붙이는거는 필수는 아니지만, 세미콜론을 붙이는 것을 매우 권장한다.

---

### JavaScript White Space

### 자바스크립트 여백

JavaScript ignores multiple spaces. You can add white space to your script to make it more readable.  
The following lines are equivalent:

자바스크립트는 다수의 공백을 제외합니다. 당신이 잘 읽을수 있도록 여백을 추가할 수 있습니다.  
다음에 나오는 줄의 의미는 같습니다:

<pre class="prettyprint">
var person = "Hege";
var person="Hege";
</pre>

A good practice is to put spaces around operators ( = + - * / ):  
좋은 방법은 연산자의 주위를 공백을 넣는 것 입니다.

var x = y + z;

---

### JavaScript Line Length and Line Breaks

### 자바스크립트 줄 길이와 줄바꿈

For best readability, programmers often like to avoid code lines longer than 80 characters.   
If a JavaScript statement does not fit on one line, the best place to break it, is after an operator:

최고의 가독성을 위해서, 프로그램 라인의 길이가 80자인 코드를 피하는 것입니다.  
만약 자바스크립트 문이 한줄에 끝나지 않는경우에, 더좋은 방법은 연산자에서 줄바꿈 입니다.

<pre class="prettyprint">
Example
document.getElementById("demo").innerHTML = 
"Hello Dolly.";
</pre>

---

### JavaScript Code Blocks

### 자바스크립트 코드묶음

JavaScript statements can be grouped together in code blocks, inside curly brackets {...}.   
The purpose of code blocks is to define statements to be executed together.   
One place you will find statements grouped together in blocks, are in JavaScript functions:

자바스크립트문은 {...}내부 코드로 묶어 그룹화 할 수 있습니다.  
코드 묶음의 목적은 문장이 같이 실행되는 것을 정의합니다.  
자바스크립트 함수 장소 안에서 당신이 그룹화한 문장을 찾을수 있습니다.

<pre class="prettyprint">
Example
function myFunction() {
    document.getElementById("demo").innerHTML = "Hello Dolly.";
    document.getElementById("myDIV").innerHTML = "How are you?";
}
</pre>

In this tutorial we use 4 spaces of indentation for code blocks.  
You will learn more about functions later in this tutorial.

이 튜토리얼에서 우리는 코드불록 들여 쓰기 4공간을 사용했습니다.  
우리는 더 많은 함수의 기능을 다음에 자세하게 배울 것 입니다.

---

### JavaScript Keywords

### 자바스크립트 핵심

JavaScript statements often start with a keyword to identify the JavaScript action to be performed.   
Here is a list of some of the keywords you will learn about in this tutorial:  
 
자바스크립트에서 자주 쓰이는 핵심적인 자바스크립트의 실행방법을 확인해 봅시다.  
다음 튜토리얼에서 배울 일부 핵심 목록 입니다. 

* break: Terminates a switch or a loop
* continue: Jumps out of a loop and starts at the top
* debugger: Stops the execution of JavaScript, and calls (if available) the debugging function
* do ... while: Executes a block of statements, and repeats the block, while a condition is true
* for: Marks a block of statements to be executed, as long as a condition is true
* function: Declares a function
* if ... else: Marks a block of statements to be executed, depending on a condition
* return: Exits a function
* switch: Marks a block of statements to be executed, depending on different cases
* try ... catch: Implements error handling to a block of statements
* var: Declares a variable

* break: 스위치나 루프 종료합니다.
* continue: 루프 점프나 위에서 시작합니다.
* debugger: 자바스크립트의 실행을 중지하고 디버그 함수를 호출합니다.
* do ... while: 조건이 true인 동안에 묶음 문장을 실행하고 묶음을 반복합니다.
* for: 명령문 블록이 실행되는 동안에 true상태이기만 하면 실행 됩니다.
* function: 함수를 선언합니다.
* if ... else: 표시된 문장 블록 조건에 따라 실행됩니다.
* return: 기능 종료합니다.
* switch: 표시된 문장 블록은 경우에 따라 실행됩니다.
* try ... catch: 문장 블록에 오류처리합니다.
* var: 변수 선언합니다.

JavaScript keywords are reserved words. Reserved words cannot be used as names for variables.  

자바스크립트 키워드는 단어의 예약입니다. 예약어는 변수 이름으로 사용할 수 없습니다.

---

---

# JavaScript Comments

# 자바스크립트 주석

---

JavaScript comments can be used to explain JavaScript code, and to make it more readable.   
JavaScript comments can also be used to prevent execution, when testing alternative code.

자바스크립트 주석은 자바스크립트 코드를 설명하는데 사용하거나 가독성을 위해 사용합니다.  
자바스크립트 주석은 코드를 테스트를 하거나 보이지 않게 하기위해서 사용이 가능합니다.

---

### Single Line Comments

### 각 줄의 주석

Single line comments start with //.   
Any text between // and the end of the line, will be ignored by JavaScript (will not be executed).   
This example uses a single line comment before each line, to explain the code:

각 줄의 주석의 시작은 //로 합니다.  
// 와 줄의 끝 사이에 글은 자바스크립트에서 제외됩니다.(제거하여 보이지 않는다.)  
이 예제는 각줄의 주석을 줄 앞에 사용하는 것을 설명하는 코드 예제 입니다.

<pre class="prettyprint">
Example
// Change heading:
document.getElementById("myH").innerHTML = "My First Page";
// Change paragraph:
document.getElementById("myP").innerHTML = "My first paragraph.";
</pre>

This example uses a single line comment at the end of each line, to explain the code:   
이 예제는 하나의 줄에 주석은 줄의 끝까지 인것을 설명하는 코드 입니다. :

<pre class="prettyprint">
Example
var x = 5;      // Declare x, give it the value of 5
var y = x + 2;  // Declare y, give it the value of x + 2
</pre>

---

### Multi-line Comments

### 여러줄의 주석

<pre class="prettyprint">
Multi-line comments start with /* and end with */.   
Any text between /* and */ will be ignored by JavaScript.  
This example uses a multi-line comment (a comment block) to explain the code:

여러줄의 주석의 시작은 /* 로 시작하여 */로 끝납니다.  
이것은 /* 와 */ 사이에 문자는 자바스크립트에서 제외됩니다.  
여러줄에 주석 사용에 대한 설명을 한 예제 코드입니다.(주석 묶음)
</pre>

<pre class="prettyprint">
Example
/*
The code below will change
the heading with id = "myH"
and the paragraph with id = "myP"
in my web page:
*/
document.getElementById("myH").innerHTML = "My First Page";
document.getElementById("myP").innerHTML = "My first paragraph.";
</pre>

It is most common to use single line comments.  
Block comments are often used for formal documentation.

이것은 흔히 사용하는 단독 주석입니다.  
묶음 주석은 종종 공식 문서에 사용됩니다.

---

### Using Comments to Prevent Execution

### 실행 방지를 위한 주석사용

Using comments to prevent execution of code, is suitable for code testing.  
Adding // in front of a code line changes the code lines from an executable line to a comment.   
This example uses // to prevent execution of one of the code lines:
 
적절한 코드에 대한 테스트를 위해서 주석을 사용해서 코드의 실행을 방지할 수 있습니다.  
변경될 코드 앞에 // 를 추가해서 주석으로 실행할 수 있습니다.  
이 예제는 //로 한줄의 실행을 방지한 코드 입니다.:

<pre class="prettyprint">
Example
//document.getElementById("myH").innerHTML = "My First Page";
document.getElementById("myP").innerHTML = "My first paragraph.";
</pre>

This example uses a comment block to prevent execution of multiple lines:  
이 예제는 주석을 묶음단위로 사용하여 여러줄의 실행을 방지한 것 입니다:

<pre class="prettyprint">
Example
/*
document.getElementById("myH").innerHTML = "My First Page";
document.getElementById("myP").innerHTML = "My first paragraph.";
*/
</pre>

---

---

# JavaScript Variables

# 자바스크립트 변수

### JavaScript Variables

### 자바스크립트 변수

JavaScript variables are containers for storing data values.  
In this example, x, y, and z, are variables:

자바스크립트 변수는 컨테이너에 데이터 값을 저장하는 것입니다.    
x,y,z에 대한 변수 예제 입니다.

<pre class="prettyprint">
Example
var x = 5;
var y = 6;
var z = x + y;
</pre>

From the example above, you can expect:

당신은 위에서 본 예제에서 예상할 수 있을 것입니다.

* x stores the value 5    
* y stores the value 6  
* z stores the value 11  

* x에 5값을 저장
* y에 6값을 저장
* z에 11값을 저장

---

### Much Like Algebra

### 수학과 많이 비슷합니다.

In this example, price1, price2, and total, are variables:

에제 안에는 price1, price2, total의 변수 입니다:

<pre class="prettyprint">
Example
var price1 = 5;
var price2 = 6;
var total = price1 + price2;
</pre>

In programming, just like in algebra, we use variables (like price1) to hold values.    
In programming, just like in algebra, we use variables in expressions (total = price1 + price2).  
From the example above, you can calculate the total to be 11.  
JavaScript variables are containers for storing data values.

우리는 프로그램안에서 그냥 변수에 수를 넣어서 수학적으로 사용합니다.  
우리는 프로그램안에서 변수를 수학적으로 표현합니다. 

---

### JavaScript Identifiers

### 자바스크립트 식별자

All JavaScript variables must be identified with unique names.   
These unique names are called identifiers.   
Identifiers can be short names (like x and y), or more descriptive names (age, sum, totalVolume).   
The general rules for constructing names for variables (unique identifiers) are:  

모든 자바스크립트 변수는 고유의 식별자 이름을 필요로 합니다.  
식별자 이름은 고유이름으로 불립니다.  
식별자는 짧은 x나y처럼 짧은 이름이나 무언가를 설명하는 age,sum,totalVolume으로도 사용이 사능합니다.  
일반적인 규칙은 변수는 고유의 식별자 이름으로 구성됩니다:

* Names can contain letters, digits, underscores, and dollar signs.
* Names must begin with a letter
* Names can also begin with $ and _ (but we will not use it in this tutorial)
* Names are case sensitive (y and Y are different variables)
* Reserved words (like JavaScript keywords) cannot be used as names

* 이름안에는 달러나, 알파벳이나, 수학기호나, 밑줄로 사용이 가능합니다.
* 이름을 시작할때는 영문으로 시작합니다.
* 이름은 달러나 _로도 시작이 가능합니다.(하지만 우리 튜토리얼에서는 사용하지 않습니다)
* 이름으로는 대소문자를 구분합니다(Y와y는 다른변수 입니다)
* 자바스크립트의 핵심과 맞는 것을 이름으로 사용합니다.

JavaScript identifiers are case-sensitive.

스크립트는 식별자는 대소문자를 구별합니다.

---

### The Assignment Operator

### 할당 연산자

In JavaScript, the equal sign (=) is an "assignment" operator, not an "equal to" operator.   
This is different from algebra. The following does not make sense in algebra:

자바스크립트의 = 는 같다는 의미의 연산자가 아닌 할당 연산자 입니다.

<pre class="prettyprint">
x = x + 5
</pre>

In JavaScript, however, it makes perfect sense: it assigns the value of x + 5 to x.   
(It calculates the value of x + 5 and puts the result into x. The value of x is incremented by 5.)

자바스크립트 안에서는 정확하게 x + 5의 값을 x에 할당합니다.  
이것은 수학적인 것과 다릅니다. 다음에 나오는 것은 수학적으로 판달하지

The "equal to" operator is written like == in JavaScript.

자바스크립트 에서는 같다는 표시를 == 로 쓰여집니다.

---

### JavaScript Data Types

### 자바스크립트 데이터 형식

JavaScript variables can hold numbers like 100, and text values like "John Doe".  
In programming, text values are called text strings.  
JavaScript can handle many types of data, but for now, just think of numbers and strings.   
Strings are written inside double or single quotes. Numbers are written without quotes.   
If you put quotes around a number, it will be treated as a text string.

자바스크립트 변수는 숫자는 100으로, 문자 값은 "John Doe"으로 할 수 있습니다.  
프로그래밍 안에서 문자값은 문자열로 불립니다.  
자바스크립트는 많은 형식의 데이터를 다룰수 있습니다, 하지만 지금은 숫자와 문자열만 생각하겠습니다.  
문자열은 쌍따옴표 사이에 문자가 쓰입니다. 숫자는 따옴표 없이 쓰여집니다.  
만약 당신이 따옴표에 숫자를 넣었으면 그것은 문자열로 취급될 것 입니다.

<pre class="prettyprint">
Example
var pi = 3.14;
var person = "John Doe";
var answer = 'Yes I am!';
</pre>

---

### Declaring (Creating) JavaScript Variables

### 자바스크립트 변수 선언(변수를 만들다)

Creating a variable in JavaScript is called "declaring" a variable.  
You declare a JavaScript variable with the var keyword:

자바스크립트에서는 변수를 선언해서 변수를 만들수 있습니다.  
당신은 자바스크립트 변수를 var keyword에 선언합니다. 

<pre class="prettyprint">
var carName;
</pre>

After the declaration, the variable has no value. (Technically it has the value of undefined)   
To assign a value to the variable, use the equal sign:

선언 했던것은, 값이 없는 변수 입니다.(말하자면 값이 의미를 가지고 있지 않다)  
변수에 값을 할당할때는 =를 사용합니다.

<pre class="prettyprint">
carName = "Volvo";
</pre>

You can also assign a value to the variable when you declare it:  

당신은 변수를 선언할때 값을 넣는것이 가능합니다.

<pre class="prettyprint">
var carName = "Volvo";
</pre>

In the example below, we create a variable called carName and assign the value "Volvo" to it.  
Then we "output" the value inside an HTML paragraph with id="demo":

아래 예제는 우리가 carName으로 불리는 것과 값으로 "Volvo"라고 넣어서 만들 변수 입니다.  
그것은 우리가 HTML paragraph with id="demo"안에다가 값을 넣어야 출력 됩니다.

<pre class="prettyprint">
Example
&lt;p id="demo"&gt;&lt;/p&gt;

&lt;script&gt;
var carName = "Volvo";
document.getElementById("demo").innerHTML = carName; 
&lt;/script&gt;
</pre>

It's a good programming practice to declare all variables at the beginning of a script.  

스크립트가 시작할때 변수를 선언하는 것이 좋은 프로그래밍 입니다.

---

### One Statement, Many Variables

### 하나의 문장, 많은 변수

You can declare many variables in one statement.  
Start the statement with var and separate the variables by comma:

당신은 하나의 문장에 많은 변수를 선언하는 것이 가능 합니다.  
문장을 시작할때 변수에 콤마로 var의 구역을 나눌수 있습니다.

<pre class="prettyprint">
var person = "John Doe", carName = "Volvo", price = 200;
</pre>

A declaration can span multiple lines:  

새로운 여러줄에다가 선언하는게 가능합니다.

<pre class="prettyprint">
var person = "John Doe",
carName = "Volvo",
price = 200;
</pre>

### Value = undefined

### 값 = 정의되지 않다

In computer programs, variables are often declared without a value. The value can be something that has to be calculated, or something that will be provided later, like user input.  
A variable declared without a value will have the value undefined.  
The variable carName will have the value undefined after the execution of this statement:

컴퓨터 프로그램 안에서는, 변수는 값이 없이 자주 선언됩니다. 계산되어야 하는 값이나 사용자의 입력 같은것은 나중에 제공하는 것이 가능합니다.  
선언한 변수는 값이 없으면 값이 정의되지 않습니다.  
명령문을 실행하면 변수 carName의 값이 정의되지 않는 값으로 실행 될 것입니다.

<pre class="prettyprint">
Example
var carName;
</pre>

---

### Re-Declaring JavaScript Variables

### 자바스크립트 변수를 다시 정의합니다.

If you re-declare a JavaScript variable, it will not lose its value.   
The variable carName will still have the value "Volvo" after the execution of these statements:

만약 자바스크립트변수를 다시선언을 해도 값을 잃어버리진 않을 것 입니다.   
변수carName는 계속해서 값으로 "Volvo"를 가지고 문장이 실행 될 것입니다.  

<pre class="prettyprint">
Example
var carName = "Volvo";
var carName;
</pre>

---

### JavaScript Arithmetic

### 자바스크립트 계산

As with algebra, you can do arithmetic with JavaScript variables, using operators like = and +:

당신은 수학처럼 자바스크립트의 변수에 = 와 + 같은 것들로 계산을 하는 것이 가능합니다.

<pre class="prettyprint">
Example
var x = 5 + 2 + 3;
</pre>

You can also add strings, but strings will be concatenated (added end-to-end):

게다가 당신은 문자열을 추가하면 문자열이 연결되어 집니다.

<pre class="prettyprint">
Example
var x = "John" + " " + "Doe";
</pre>

Also try this:  

이것도 시도해 봅니다:

<pre class="prettyprint">
Example
var x = "5" + 2 + 3;
</pre>

If you add a number to a string, the number will be treated as string, and concatenated.

만약 당신이 숫자에 문자열을 추가하게 된다면, 그 숫자들은 문자열로 취급되어서 연결되어 나오게 됩니다.

---

### Test Yourself with Exercises!

[[실습1](http://www.w3schools.com/js/exercise.asp?filename=exercise_variables1)]
[[실습2](http://www.w3schools.com/js/exercise.asp?filename=exercise_variables2)]
[[실습3](http://www.w3schools.com/js/exercise.asp?filename=exercise_variables3)]
[[실습4](http://www.w3schools.com/js/exercise.asp?filename=exercise_variables4)]
[[실습5](http://www.w3schools.com/js/exercise.asp?filename=exercise_variables5)]
[[실습6](http://www.w3schools.com/js/exercise.asp?filename=exercise_variables6)]

---

---

# JavaScript Operators 

# 자바스크립트 연산자

---

<pre class="prettyprint">
Example
Assign values to variables and add them together:

var x = 5;         // assign the value 5 to x
var y = 2;         // assign the value 2 to y
var z = x + y;     // assign the value 7 to z (x + y)
</pre>

---

### JavaScript Arithmetic Operators

Arithmetic operators are used to perform arithmetic on numbers (literals or variables).  

연산자의 연산은 (문자 그대로의)숫자를 계산하는데 사용합니다.

<pre class="prettyprint">
Operator	Description  
+ 		Addition 	 덧셈
- 		Subtraction   	 뺄셈
* 		Multiplication 	 곱셈
/ 		Division 	 나눗셈
%		Modulus  	 계수
++ 		Increment 	 증가
-- 		Decrement 	 감소
The addition operator (+) adds numbers:  
덧셈 연산자는 숫자를 더합니다:
</pre>

<pre class="prettyprint">
Adding
var x = 5;
var y = 2;
var z = x + y;
</pre>

The multiplication operator (*) multiplies numbers.  
곱셈연산자는 숫자를 곱합니다:

<pre class="prettyprint">
Multiplying
var x = 5;
var y = 2;
var z = x * y;
</pre>

You will learn more about JavaScript operators in the next chapters.  
당신은 더많은 자바스크립트의 연산자에 대해서 다음장에서 배울것 입니다.

---

### JavaScript Assignment Operators

### 자바스크립트 할당 연산자

Assignment operators assign values to JavaScript variables.

할당 연산자는 자바스크립트의 변수에 값을 할당합니다.

<pre class="prettyprint">
Operator	Example		Same As
=		x = y		x = y
+=		x += y		x = x + y
-=		x -= y		x = x - y
*=		x *= y		x = x * y
/=		x /= y		x = x / y
%=		x %= y		x = x % y

The assignment operator (=) assigns a value to a variable.  
그할당 연산자는 변수에 값을 = 로 할당합니다.

Assignment  할당

var x = 10;

The addition assignment operator (+=) adds a value to a variable.  
덧셈 할당 연산자는 변수에 값을 더합니다.

Assignment  할당

var x = 10;
x += 5;
</pre>

---

### JavaScript String Operators

### 자바스크립트 문자열 연산자

The + operator can also be used to add (concatenate) strings.   
When used on strings, the + operator is called the concatenation operator.

+연산자는 문자열을 더하는데 사용이 가능합니다.  
문자열에 +연산자를 사용하면 연결연산자 라고 불립니다.

<pre class="prettyprint">
Example
txt1 = "John";
txt2 = "Doe";
txt3 = txt1 + " " + txt2;

The result of txt3 will be:  
txt3에 대한 결과입니다.:

John Doe

The += assignment operator can also be used to add (concatenate) strings:  
+=할당 연산자는 문자열을 추가(연결)하여 사용하는게 가능합니다.

Example
txt1 = "What a very ";
txt1 += "nice day";

The result of txt1 will be:   
txt1에 대한 결과 입니다.:  

What a very nice day

</pre>

---

### Adding Strings and Numbers

### 문자열과 숫자의 덧셈

Adding two numbers, will return the sum, but adding a number and a string will return a string:

두개의 숫자의 합을 반환 하거나, 숫자나와 문자열을 더하면 문자열로 반환합니다: 

<pre class="prettyprint">
Example
x = 5 + 5;
y = "5" + 5;
z= "Hello" + 5;

The result of x, y, and z will be:  
x,y,z에 대한 결과입니다:

10
55
Hello5
</pre>

The rule is: If you add a number and a string, the result will be a string!  
규칙 : 만약 당신이 숫자와 문자를 더하면 그 결과는 문자열 입니다!

---

### JavaScript Comparison and Logical Operators

### 자바스크립트 비교와 논리적인 연산자

<pre class="prettyprint">
Operator	Description  
==		equal to  				같다
===		equal value and equal type  		값과 타입이 같다
!=		not equal  				같지 않다
!==		not equal value or not equal type 	값또는 타입이 같지않다  
&gt;		greater than  				보다 크다
&lt;		less than  				보다 작다
&gt;=		greater than or equal to  		보다 크거나 같다
&lt;=		less than or equal to  			보다 작거나 같다
</pre>

Comparison and logical operators are described in the JS Comparisons chapter.

비교와 논리적인 연산자는 JS Comparisons장에서 설명하겠습니다.

---

---

# JavaScript Arithmetic

# 자바스크립트 계산

---

A typical thing to do with numbers is arithmetic.  

전형적인 숫자 계산 방법

---

### JavaScript Arithmetic Operators

### 자바스크립트 연산자

Arithmetic operators perform arithmetic on numbers (literals or variables).  

계산 연산자는 (상수나 변수)숫자를 계산합니다

<pre class="prettyprint">
Operator	Description  
+		Addition  	덧셈
-		Subtraction  	뺄셈
*		Multiplication  곱셈
/		Division  	나눗셈
%		Modulus  	계수
++		Increment  	증가
--		Decrement  	감소
</pre>

---

### Arithmetic Operations

### 연산자 계산

A typical arithmetic operation operates on two numbers.   
The two numbers can be literals:  

전형적인 계산을 진행할 때는 두개의 숫자로 진행합니다.  
두개의 상수로 가능합니다

<pre class="prettyprint">
Example
var x = 100 + 50;
</pre>

or variables: 또는 변수로

<pre class="prettyprint">
Example
var x = a + b;
</pre>

or expressions: 다른 식

<pre class="prettyprint">
Example
var x = (100 + 50) * a;
</pre>

---

### Operators and Operands

### 피연산자 와 연산자

The numbers (in an arithmetic operation) are called operands.   
The operation (to be performed between the two operands) is defined by an operator.  

숫자(연산)는 피연산자 라고 불려집니다.  
(두 피연산자 사이에 실행될)동작을 연산자로 정의합니다.  

<pre class="prettyprint">
Operands	Operators	Operand
100		+		50
</pre>

The addition operator (+) adds numbers:   
덧셈 연산자는 숫자를 더합니다.

<pre class="prettyprint">
Adding
var x = 5;
var y = 2;
var z = x + y;
</pre>

The subtraction operator (-) subtracts numbers.  
뺄셈 연산자는 숫자를 뺍니다.

<pre class="prettyprint">
Subtracting
var x = 5;
var y = 2;
var z = x - y;
</pre>

The multiplication operator (*) multiplies numbers.  
곱셈 연산자는 숫자를 곱합니다.

<pre class="prettyprint">
Multiplying
var x = 5;
var y = 2;
var z = x * y;
</pre>

The division operator (/) divides numbers.  
나눗셈 연산자는 숫자를 나눕니다.

<pre class="prettyprint">
Dividing
var x = 5;
var y = 2;
var z = x / y;
</pre>

The modular operator (%) returns the division remainder.   
모듈러 연산자는 분할된 나머지를 반환합니다.

<pre class="prettyprint">
Modulus
var x = 5;
var y = 2;
var z = x % y;
</pre>

The increment operator (++) increments numbers.  
증가 연산자는 숫자를 증가시킵니다.

<pre class="prettyprint">
Incrementing
var x = 5;
x++;
var z = x;
</pre>

The decrement operator (- -) decrements numbers.   
감소 연산자는 숫자를 감소시킵니다.

<pre class="prettyprint">
Decrementing
var x = 5;
x--;
var z = x;
</pre>

---

### Operator Precedence

### 연산자 순서

Operator precedence describes the order in which operations are performed in an arithmetic expression.

연산자 우선순위에 따른 연산 순서에 대해서 설명합니다.

<pre class="prettyprint">
Example
var x = 100 + 50 * 3;
</pre>

Is the result of example above the same as 150 * 3, or is it the same as 100 + 150?  
Is the addition or the multiplication done first?  
As in traditional school mathematics, the multiplication is done first.   
Multiplication (*) and division (/) have higher precedence than addition (+) and subtraction (-).   
And (as in school mathematics) the precedence can be changed by using parentheses:

위의 예제와 같은 결과는 150 * 3 또는 100 + 150과 같습니까? 
덧셈과 곱셈중 어떤것이 먼저일까?  
전형적인 학교 수학에서는, 곱셈을 먼저 합니다.  
곱셈과 나눗셈은 덧셈과 뺄셈보다 우선 순위 입니다.  
그리고 학교 수학에서처럼 괄호로 우선순위를 바꿀 수 있습니다.

<pre class="prettyprint">
Example
var x = (100 + 50) * 3;
</pre>

When using parentheses, the operations inside the parentheses are computed first.    
When many operations have the same precedence (like addition and subtraction), they are computed from left to right:

괄호를 사용할때, 연산자는 괄호 안을 먼저 계산을 합니다.  
덧셈과 뺄셈처럼 연산의 우선순위가 같을경우에는 왼쪽에서 오른쪽으로 계산합니다.

<pre class="prettyprint">
Example
var x = 100 + 50 - 3;
</pre>

---

### JavaScript Operator Precedence Values

### 자바스크립트 연산자 값의 우선순위

<pre class="prettyprint">
Value	Operator	Description		Example
19	( )		Expression grouping	(3 + 4)
 	 	 	 
18	.		Member			person.name
18	[]		Member			person["name"]
 	 	 	 
17	()		Function call		myFunction()
17	new		Create			new Date()
 	 	 	 
16	++		Postfix Increment	i++
16	--		Postfix Decrement	i--
 	 	 	 
15	++		Prefix Increment	++i
15	--		Prefix Decrement	--i
15	!		Logical not		!(x==y)
15	typeof		Type			typeof x
 	 	 	 
14	*		Multiplication		10 * 5
14	/		Division		10 / 5
14	%		Modulo division		10 % 5
14	**		Exponentiation		10 ** 2
 	 	 	 
13	+		Addition		10 + 5
13	-		Subtraction		10 - 5
 	 	 	 
12	&lt;&lt;		Shift left		x &lt;&lt; 2
12	&gt;&gt;		Shift right		x &gt;&gt; 2
 	 	 	 
11	&lt;		Less than		x &lt; y 
11	&lt;=		Less than or equal	x &lt;= y
11	&gt;		Greater than		x &gt; y
11	&gt;=		Greater than or equal	x &gt;= y
 	 	 	 
10	==		Equal			x == y
10	===		Strict equal		x === y
10	!=		Unequal			x != y
10	!==		Strict unequal		x !== y
 	 	 	 
6	&&		And			x && y
5	||		Or			x || y
 	 	 	 
3	=		Assignment		x = y
3	+=		Assignment		x += y
3	-=		Assignment		x -= y
3	*=		Assignment		x *= y
3	/=		Assignment		x /= y
</pre>

Expressions in parentheses are fully computed before the value is used in the rest of the expression.

다른 식을 계산하기 전에 괄호를 완전히 계산하고 나머지 식을 계산합니다.

---

Test Yourself with Exercises!

스스로 연습문제 테스트

[[연습문제1](http://www.w3schools.com/js/exercise.asp?filename=exercise_arithmetic1)]
[[연습문제2](http://www.w3schools.com/js/exercise.asp?filename=exercise_arithmetic2)]
[[연습문제3](http://www.w3schools.com/js/exercise.asp?filename=exercise_arithmetic3)]
[[연습문제4](http://www.w3schools.com/js/exercise.asp?filename=exercise_arithmetic4)]
[[연습문제5](http://www.w3schools.com/js/exercise.asp?filename=exercise_arithmetic5)]

---

---

# JavaScript Assignment

# 자바스크립트 할당

### JavaScript Assignment Operators

### 자바스크립트 할당 연산자

Assignment operators assign values to JavaScript variables.

할당 연산자는 자바스크립트 변수에 값을 할당합니다.

<pre class="prettyprint">
Operator	Example		Same As
=		x = y		x = y
+=		x += y		x = x + y
-=		x -= y		x = x - y
*=		x *= y		x = x * y
/=		x /= y		x = x / y
%=		x %= y		x = x % y
</pre>

The = assignment operator assigns a value to a variable.

=할당 연산자로 변수에 값을 할당합니다.

<pre class="prettyprint">
Assignment
var x = 10;
</pre>

The += assignment operator adds a value to a variable.

+=할당 연산자는 변수에 값을 추가하여 할당합니다.

<pre class="prettyprint">
Assignment
var x = 10;
x += 5;
</pre>

The -= assignment operator subtracts a value from a variable.

-=할당 연산자는 변수에 값을 뺄셈하여 할당합니다.

<pre class="prettyprint">
Assignment
var x = 10;
x -= 5;
</pre>

The *= assignment operator multiplies a variable.

*=할당 연산자는 변수를 곱합니다.

<pre class="prettyprint">
Assignment
var x = 10;
x *= 5;
</pre>

The /= assignment divides a variable.

/=할당 연산자는 변수를 나눕니다.

<pre class="prettyprint">
Assignment
var x = 10;
x /= 5;
</pre>

The %= assignment operator assigns a remainder to a variable.

%=할당 연산자는 변수에 나머지 값을 할당합니다.

<pre class="prettyprint">
Assignment
var x = 10;
x %= 5;
</pre>

---

### Test Yourself with Exercises!

### 스스로 연습문제 시험

[[연습문제1](http://www.w3schools.com/js/exercise.asp?filename=exercise_assignment1)]
[[연습문제2](http://www.w3schools.com/js/exercise.asp?filename=exercise_assignment2)]
[[연습문제3](http://www.w3schools.com/js/exercise.asp?filename=exercise_assignment3)]
[[연습문제4](http://www.w3schools.com/js/exercise.asp?filename=exercise_assignment4)]
[[연습문제5](http://www.w3schools.com/js/exercise.asp?filename=exercise_assignment5)]

---

---

# JavaScript Data Types

# 자바스크립트 데이터 형식

---

String, Number, Boolean, Array, Object.  

문자열, 숫자, 논리형, 배열, 객체

---

### JavaScript Data Types

### 자바스크립트 데이터 형식

JavaScript variables can hold many data types: numbers, strings, arrays, objects and more:  

자바스크립트 변수들은 많은 데이터 형식들을 가지고 있습니다: 숫자, 문자열, 배열, 객체 와 더많은 것을:

<pre class="prettyprint">
var length = 16;                               // Number
var lastName = "Johnson";                      // String
var cars = ["Saab", "Volvo", "BMW"];           // Array
var x = {firstName:"John", lastName:"Doe"};    // Object
</pre>

---

### The Concept of Data Types.

### 데이터 형식의 개념

In programming, data types is an important concept.   
To be able to operate on variables, it is important to know something about the type.  
Without data types, a computer cannot safely solve this:   

프로그램에서는 데이터형식의 개념이 중요합니다.  
변수를 동작할 수 있는, 어떤 유형에 대한 데이터 타입을 아는것이 중요합니다.  
데이터 타입이 없이는, 컴퓨터는 안전하게 그것을 해결할 수 없습니다.

<pre class="prettyprint">
var x = 16 + "Volvo";
</pre>

Does it make any sense to add "Volvo" to sixteen? Will it produce an error or will it produce a result?   
JavaScript will treat the example above as:  

"Volvo"에 16을 추가한다는 것이 감이 오시나요? 그것은 에러를 발생시키거나 어떤 결과를 만들어 내나요?  
자바스크립트 위에 예제를 다음과 같이 처리합니다.

<pre class="prettyprint">
var x = "16" + "Volvo";
</pre>

When adding a number and a string, JavaScript will treat the number as a string.  
자바스크립트는 문자열과 숫자열을 더하면 숫자를 문자로 처리합니다.

<pre class="prettyprint">
Example
var x = 16 + "Volvo";

Example
var x = "Volvo" + 16;
</pre>

JavaScript evaluates expressions from left to right. Different sequences can produce different results:

자바스크립트 왼쪽에서 오른쪽으로 식을 평가합니다. 연속적인다른 순서는 다른 결과를 만들어 냅니다.

<pre class="prettyprint">
JavaScript:
var x = 16 + 4 + "Volvo";
Result:
20Volvo

JavaScript:
var x = "Volvo" + 16 + 4;
Result:
Volvo164
</pre>

In the first example, JavaScript treats 16 and 4 as numbers, until it reaches "Volvo".   
In the second example, since the first operand is a string, all operands are treated as strings.

"Volvo"까지 도달하는 첫번째 예제는, 자바스크립트는 16부터 4까지는 숫자로 다루어 집니다.  
두번째 예제는, 첫번째에서 문자열을 연산하면은, 모두 문자열로 다루어 집니다.

---

### JavaScript Has Dynamic Types

### 자바스크립트는 동적인 형식을 가지고 있습니다.

JavaScript has dynamic types. This means that the same variable can be used as different types:  

자바스크립트는 동적인 형식을 가지고 있습니다. 이 의미는 변수에 다른 형식을 사용할 수 있다는 것을 의미합니다.

<pre class="prettyprint">
Example
var x;               // Now x is undefined
var x = 5;           // Now x is a Number
var x = "John";      // Now x is a String
</pre>

---

### JavaScript Strings

### 자바스크립트 문자열

A string (or a text string) is a series of characters like "John Doe".   
Strings are written with quotes. You can use single or double quotes:

"John Doe"와 같은 문자열(또는 문자) 입니다.  
문자열은 따옴표를 사용합니다. 당신은 따옴표나 쌍따옴표를 사용합니다.


<pre class="prettyprint">
Example
var carName = "Volvo XC60";   // Using double quotes
var carName = 'Volvo XC60';   // Using single quotes
</pre>

You can use quotes inside a string, as long as they don't match the quotes surrounding the string:

당신은 따옴표 안의 문자열과 문자열 주변의 따옴표가 다르기만 하면 그것들을 사용할 수 있습니다.

<pre class="prettyprint">
Example
var answer = "It's alright";             // Single quote inside double quotes
var answer = "He is called 'Johnny'";    // Single quotes inside double quotes
var answer = 'He is called "Johnny"';    // Double quotes inside single quotes
</pre>

You will learn more about strings later in this tutorial.  

당신은 다음 튜토리얼에서 더많은 문자열에 대해서 배울 것 입니다.

---

### JavaScript Numbers

### 자바스크립트 숫자
 
JavaScript has only one type of numbers.  
Numbers can be written with, or without decimals:

자바스크립트는 형식중 하나로 숫자가 있습니다.  
숫자는 소수점이 없는것과 있는것으로 사용이 가능합니다.:

<pre class="prettyprint">
Example
var x1 = 34.00;     // Written with decimals
var x2 = 34;        // Written without decimals
</pre>

Extra large or extra small numbers can be written with scientific (exponential) notation:

더 크거나, 작은 숫자들은 (지수)로 표기하는 방법을 사용할 수 있습니다.

<pre class="prettyprint">
Example
var y = 123e5;      // 12300000
var z = 123e-5;     // 0.00123
</pre>

You will learn more about numbers later in this tutorial.

다음 튜토리얼에서 더많은 숫자에 대해서 배울 것 입니다.

---

### JavaScript Booleans

### 자바스크립트 논리형

Booleans can only have two values: true or false.

논리형은 오직 참 과 거짓 같만 가지고 있습니다.

<pre class="prettyprint">
Example
var x = true;
var y = false;
</pre>

Booleans are often used in conditional testing.   
You will learn more about conditional testing later in this tutorial.  

논리형은 흔히 조건부 테스트 할때 사용됩니다.  
당신은 다음 튜토리얼에서 더많은 조건부 테스트에 대해서 배우게 될 것 입니다.

---

### JavaScript Arrays

### 자바스크립트 배열

JavaScript arrays are written with square brackets.  
Array items are separated by commas.  
The following code declares (creates) an array called cars, containing three items (car names):

자바스크립트 배열은 대괄호로 사용합니다.  
배열의 항목들은 콤마로 구분합니다.  
다음으로 나오는 코드는 car로 불리는 배열을 선언하여 만들 것 이고, 3개의 항목 (차이름)이 들어가 있습니다.

<pre class="prettyprint">
Example
var cars = ["Saab", "Volvo", "BMW"];
</pre>

Array indexes are zero-based, which means the first item is [0], second is [1], and so on.   
You will learn more about arrays later in this tutorial.

배열의 인덱스는 첫번째 항목은[0]이고 두번째는[1]로 0을 기반으로 합니다.  
당신은 다음 튜토리얼에서 더많은 배열에 대해서 배우게 될 것 입니다.  

---

### JavaScript Objects

### 자바스크립트 객체

JavaScript objects are written with curly braces.  
Object properties are written as name:value pairs, separated by commas.

자바스크립트 객체는 중괄호를 사용합니다.  
객체는 객체의 속성에 대한 이름:값을 구분할때는 콤마를 사용합니다.

<pre class="prettyprint">
Example
var person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
</pre>

The object (person) in the example above has 4 properties: firstName, lastName, age, and eyeColor.  
You will learn more about objects later in this tutorial.

위 예제에서 객체는 4개의 속성을 가지고 있습니다: firstName, lastName, age, and eyeColor.  
당신은 다음 튜토리얼에서 더많은 객체에 대해서 배우게 될 것 입니다.

---

### The typeof Operator

### 연산자 형식

You can use the JavaScript typeof operator to find the type of a JavaScript variable:

당신은 자바스크립트 연산자 형식으로 자바스크립트 변수의 에 다음과 같은 형식을 사용할 수 있습니다:

<pre class="prettyprint">
Example
typeof "John"                // Returns string 
typeof 3.14                  // Returns number
typeof false                 // Returns boolean
typeof [1,2,3,4]             // Returns object
typeof {name:'John', age:34} // Returns object
</pre>

In JavaScript, an array is a special type of object. Therefore typeof [1,2,3,4] returns object.  
자바스크립트에서 배열은 특별한 물체의 형태 입니다. 그러므로 [1,2,3,4]는 객체 형식으로 반환합니다.

---

### Undefined

### 정의되지않은

In JavaScript, a variable without a value, has the value undefined. The typeof is also undefined.

자바스크립트에서는 변수에 값이 없으면, 값으로 undefined를 가지고 있습니다. 그것은 형식도 undefined입니다.

<pre class="prettyprint">
Example
var person;                  // Value is undefined, type is undefined
</pre>

Any variable can be emptied, by setting the value to undefined. The type will also be undefined.

어떤 변수이든 undefined로 설정하여 값을 비울 수 있습니다. 그것에 대한 형식도 undefined입니다.

<pre class="prettyprint">
Example
person = undefined;          // Value is undefined, type is undefined
</pre>

---

### Empty Values

### 비어있는 값


An empty value has nothing to do with undefined.   
An empty string variable has both a value and a type.

빈값은 undefined와 관련이 없습니다.   
빈값은 값과 형식 둘다 가지고 있는 문자열 변수 입니다.

<pre class="prettyprint">
Example
var car = "";                // The value is "", the typeof is string
</pre>

---

### Null

### 가치없는

In JavaScript null is "nothing". It is supposed to be something that doesn't exist.   
Unfortunately, in JavaScript, the data type of null is an object.   
You can consider it a bug in JavaScript that typeof null is an object. It should be null.   
You can empty an object by setting it to null:  

자바스크립트에서 null은 아무것도 의미가없다. 그것은 존재하지 않는 무언가가 될 것입니다.  
불행하게도, null의 데이터 형식은 자바스크립트의 객체입니다.   
당신은 null형식이 객체인 자바스크립트 문제라고 할 수 있습니다. 그것은 null이 되야합니다.  
당신은 null로 객체를 비울 수 있습니다:

<pre class="prettyprint">
Example
var person = null;           // Value is null, but type is still an object
</pre>

You can also empty an object by setting it to undefined:  
당신은 undefined로 객체를 비울 수 있습니다.

<pre class="prettyprint">
Example
var person = undefined;     // Value is undefined, type is undefined
</pre>

### Difference Between Undefined and Null

### undefined 와 Null의 차이점

<pre class="prettyprint">
typeof undefined             // undefined
typeof null                  // object
null === undefined           // false
null == undefined            // true
</pre>

---

---

# JavaScript functions

# 자바스크립트 함수

---

A JavaScript function is a block of code designed to perform a particular task.  
A JavaScript function is executed when "something" invokes it (calls it).

자바스크립트 함수는 특정 과제를 수행하는데 필요한 코드 블록입니다.  
무언가를 호출할때 자바스크립트 기능을 호출하여 실행합니다.

---

<pre class="prettyprint">
Example
function myFunction(p1, p2) {
    return p1 * p2;              // The function returns the product of p1 and p2
}
</pre>

---

### JavaScript Function Syntax

### 자바스크립트 함수 문법

A JavaScript function is defined with the function keyword, followed by a name, followed by parentheses ().  
Function names can contain letters, digits, underscores, and dollar signs (same rules as variables).  
The parentheses may include parameter names separated by commas: (parameter1,  parameter2, ...)  
The code to be executed, by the function, is placed inside curly brackets: {}

자바스크립트 함수는 함수 키워드가 같이 정의 되며 뒤에 이름이 오고, 뒤에 괄호()가 옵니다.  
함수 이름은 문자 숫자 밑줄 달러 기호를 포함 할 수 있습니다.  
괄호는 쉼표로 구분 된 매개 변수 이름을 포함 할 수 있습니다.  
이 코드는 함수에 의해 실행되는, 중괄호 내부에{} 배치됩니다.

<pre class="prettyrpint">
function name(parameter1, parameter2, parameter3) {
    code to be executed
}
</pre>

Function parameters are the names listed in the function definition.  
Function arguments are the real values received by the function when it is invoked.  
Inside the function, the arguments behave as local variables.  
A Function is much the same as a Procedure or a Subroutine, in other programming languages.

함수name에 파라미터 명단을 열거합니다.  
함수 인수는 값이 호출 될 때 함수를 받는다. 
함수 안에 인수는 지역변수를 실행시킵니다.  
다른 프로그래밍 언어의 프로시저 또는 서브 루틴과 동일합니다.

---

### Function Invocation

### 함수 호출

The code inside the function will execute when "something" invokes (calls) the function:  

* When an event occurs (when a user clicks a button)  
* When it is invoked (called) from JavaScript code  
* Automatically (self invoked)  

You will learn a lot more about function invocation later in this tutorial.

함수안의 코드가 실행될수 있도록 호출되는 기능:

* 이벤트 발생
* 자바스크립트 코드에서 호출될 때
* 자동

나중에 튜토리얼에서 함수 호출에 대해서 더 많이 배울 것입니다.  

---

### Function Return

### 함수 반환

When JavaScript reaches a return statement, the function will stop executing.  
If the function was invoked from a statement, JavaScript will "return" to execute the code after the invoking statement.   
Functions often compute a return value. The return value is "returned" back to the "caller":

자바스크립트에 도달하면 return문은 함수의 실행을 중지합니다.  
함수가 호출된 경우에 자바스크립트 호출 문 다음 코드를 실행하기 위해 반환 합니다.  
함수들은 계산 리턴 값을 반환 값은 다시 caller를 반환 합니다.
함수는 종종 리턴값을 계산합니다. 반환되어 돌아온 값은 caller 입니다.

<pre class="prettyprint">
Example
Calculate the product of two numbers, and return the result:  
두 수의 곱을 계산해서 리턴한 결과 입니다:

var x = myFunction(4, 3);        // Function is called, return value will end up in x

function myFunction(a, b) {
    return a * b;                // Function returns the product of a and b
}

The result in x will be:  
x의 결과입니다:
12
</pre>

---

### Why Functions?

### 함수 왜 ?

You can reuse code: Define the code once, and use it many times.   
You can use the same code many times with different arguments, to produce different results.

당신은 코드를 재사용 할 수 있습니다. 한번 코드를 정의하고 그리고 여러번 사용 할 수 있습니다.  
당신은 같은 코드를 다른 곳에 사용 하여 다른 결과를 나오게 할 수 있습니다.

<pre class="prettyprint">
Example
Convert Fahrenheit to Celsius:

function toCelsius(fahrenheit) {
    return (5/9) * (fahrenheit-32);
}
document.getElementById("demo").innerHTML = toCelsius(77);
</pre>

---

### The () Operator Invokes the Function

### 연산자 함수 호출

Using the example above, toCelsius refers to the function object, and toCelsius() refers to the function result.

위의 예제를 사용하면, toCelsius는 함수 객체를 참조하고, toCelsius()은 함수 결과를 의미합니다.

<pre class="prettyprint">
Example
Accessing a function without () will return the function definition:

함수에 ()없이 반환하는 함수 정의 입니다.

function toCelsius(fahrenheit) {
    return (5/9) * (fahrenheit-32);
}
document.getElementById("demo").innerHTML = toCelsius;
</pre>

---

### Functions Used as Variables

### 변수로 사용 가능한 함수

In JavaScript, you can use functions the same way as you use variables.

당신이 자바스크립트에서 변수를 사용해서, 다음과 같은방식으로 기능을 사용할 수 있습니다.

<pre class="prettyprint">
Example
You can use:

var text = "The temperature is " + toCelsius(77) + " Celsius";

Instead of:

var x = toCelsius(32);
var text = "The temperature is " + x + " Celsius";
</pre>

You will learn a lot more about functions later in this tutorial.

나중에 튜토리얼에서 기능에대한 더 많은 것을 배울 것 입니다.

---

### Test Yourself with Exercises!

### 스스로 연습문제 테스트

[[연습문제1](http://www.w3schools.com/js/exercise.asp?filename=exercise_functions1)]
[[연습문제2](http://www.w3schools.com/js/exercise.asp?filename=exercise_functions2)]
[[연습문제3](http://www.w3schools.com/js/exercise.asp?filename=exercise_functions3)]
[[연습문제4](http://www.w3schools.com/js/exercise.asp?filename=exercise_functions4)]
[[연습문제5](http://www.w3schools.com/js/exercise.asp?filename=exercise_functions5)]

---

---

# JavaScript Objects

# 자바스크립트 객체

---

### Real Life Objects, Properties, and Methods

### 현실 객체의 성질과 방법 

In real life, a car is an object.  
A car has properties like weight and color, and methods like start and stop:

현실 안에서의 객체는 차입니다.  
차는 색상과 무게와 같은 성질이 있으며 방법으로는 시작과 정지가 있습니다: 

Object: 
![](http://www.w3schools.com/js/objectExplained.gif)

<pre class="prettyprint">
  Properties	           Methods
	
car.name = Fiat          car.start()

car.model = 500          car.drive()

car.weight = 850kg       car.brake() 
 
car.color = white        car.stop()
</pre>

All cars have the same properties, but the property values differ from car to car.  
All cars have the same methods, but the methods are performed at different times.

모든 차들은 같은 성질을 가지고 있습니다, 하지만 차들은 서로다른 값들을 가지고 있습니다.  
모든 차들은 같은 방법을 가지고 있습니다, 하지만 행동을 하는 시간을 다릅니다.

---

### JavaScript Objects

### 자바스크립트 객체

You have already learned that JavaScript variables are containers for data values.   
This code assigns a simple value (Fiat) to a variable named car:

당신은 이미 자바스크립트의 변수는 값들의 컨테이너라는 것을 배웠습니다.  
이 코드는 차라는 변수에 차 이름값을 할당한 것 입니다:

<pre class=" prettyprint">
var car = "Fiat";
</pre>

Objects are variables too. But objects can contain many values.  
This code assigns many values (Fiat, 500, white) to a variable named car:

객체도 변수 입니다. 하지만 객체는 그안에 많은 값들이 들어가는게 가능합니다.  
이 코드는 많은 차 이름에 대한 값들을 지정합니다.

<pre class="prettyprint">
var car = {type:"Fiat", model:500, color:"white"};
</pre>

The values are written as name:value pairs (name and value separated by a colon).  
JavaScript objects are containers for named values.

이름:값 쌍으로 쓰여지면서 많은 값들이 들어가는 것이 가능합니다.  
자바스크립트 객체에 이름과 값들이 들어갑니다.

---

### Object Properties

### 객체의 특성

The name:values pairs (in JavaScript objects) are called properties.

특성으로는 이름 : 값 쌍으로 (자바스크립트 객체안에서)불리어 집니다. 

<pre class="prettyprint">
var person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
</pre>

<pre class="prettyprint">
Property	Property Value
firstName	John
lastName	Doe
age		50
eyeColor	blue
</pre>

---

### Object Methods

### 객체 방법

Methods are actions that can be performed on objects.   
Methods are stored in properties as function definitions.

개체에서 수행할 수 있는 방법 입니다.  
방법 함수 정의로 속성에 저장됩니다.

<pre class="prettyprint">
Property	Property Value
firstName	John
lastName	Doe
age		50
eyeColor	blue
fullName	function() {return this.firstName + " " + this.lastName;}
</pre>

JavaScript objects are containers for named values (called properties) and methods.

자바스크립트 객체는 이름 값과 방법을 담는 컨테이너 입니다.

---

### Object Definition

### 객체의 정의

You define (and create) a JavaScript object with an object literal:

당신이 만든 자바스크립트 객체는 객체 그대로를 정의합니다.

<pre class="prettyprint">
Example
var person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
</pre>

Spaces and line breaks are not important. An object definition can span multiple lines:

객체안에서는 줄바꿈이 중요하지 않습니다. 
객체는 여러줄에서 정의 될 수도 있습니다.

<pre class="prettyprint">
Example
var person = {
    firstName:"John",
    lastName:"Doe",
    age:50,
    eyeColor:"blue"
};
</pre>

---

### Accessing Object Properties

### 개체 속성 접근

You can access object properties in two ways:

당신이 객체 속성에 접근하는 방법으로는 2가지가 있습니다.

<pre class="prettyprint">
objectName.propertyName
or
objectName["propertyName"]

Example1
person.lastName;

Example2
person["lastName"];
</pre>

---

### Accessing Object Methods

### 객체 메소드 접근

You access an object method with the following syntax:

다음으로는 당신이 객체의 메소드에 접근할수 있는 문법 입니다.

<pre class="prettyprint">
objectName.methodName()

Example
name = person.fullName();
</pre>

If you access the fullName property, without (), it will return the function definition:

만약 당신이 fullName속성에 ()없이 접근 하면 함수의 정의가 반환될 것입니다.

<pre class="prettyprint">
Example
name = person.fullName;
</pre>

---

### Do Not Declare Strings, Numbers, and Booleans as Objects!

### 객체에 문자열, 숫자, Booleans를 선언하지 않습니다.

When a JavaScript variable is declared with the keyword "new", the variable is created as an object:

자바스크립트 변수가 키워드로 선언 된 경우에는 새로운 변수가 만들어 집니다.

<pre class="prettyprint">
var x = new String();        // Declares x as a String object
var y = new Number();        // Declares y as a Number object
var z = new Boolean();       //	Declares z as a Boolean object
</pre>

Avoid String, Number, and Boolean objects. They complicate your code and slow down execution speed.   
You will learn more about objects later in this tutorial.

문자열, 숫자 및 Boolean를 피해야합니다. 그것들은 당신의 코드를 복잡하고 실행 속도를 향상 시킵니다.  
당신은 튜토리얼에서 더많은 객체에 대해서 배우게 될 것 입니다.

---

### Test Yourself with Exercises!

### 스스로 연습문제 테스트

[[연습문제1](http://www.w3schools.com/js/exercise.asp?filename=exercise_objects1)]
[[연습문제2](http://www.w3schools.com/js/exercise.asp?filename=exercise_objects2)]
[[연습문제3](http://www.w3schools.com/js/exercise.asp?filename=exercise_objects3)]

---

---

# JavaScript Scope

# 자바스크립트의 범위

---

Scope is the set of variables you have access to.

당신이 접근할 변수의 범위의 집합

---

### JavaScript Scope

### 자바스크립트의 범위

In JavaScript, objects and functions are also variables.   
In JavaScript, scope is the set of variables, objects, and functions you have access to.   
JavaScript has function scope: The scope changes inside functions.

자바스크립트 안에서 객체와 함수 또한 변수 입니다.  
자바스크립트에서 범위란 변수, 함수, 객체에 접근하는 집합 입니다.  
자바스크립트 함수의 범위 : 함수 안에서 범위를 변경합니다.

---

### Local JavaScript Variables

### 자바스크립트 지역 변수

Variables declared within a JavaScript function, become LOCAL to the function.   
Local variables have local scope: They can only be accessed within the function.

자바스크립트 함수 안에서 선언된 변수는 함수의 지역이 됩니다.  
지역 함수가 가지는 범위: 그들은 오직 함수 안에서만 접근 할 수 있습니다

<pre class="prettyprint">
Example
// code here can not use carName

function myFunction() {
    var carName = "Volvo";

    // code here can use carName

}
</pre>

Since local variables are only recognized inside their functions, variables with the same name can be used in different functions.   
Local variables are created when a function starts, and deleted when the function is completed.

이후에 지역변수는 그것들의 기능안에서 인정되고 있어서 이름이 같은 변수도 다른 기능에 사용 될 수 있습니다.  
함수가 시작할 때 지역함수가 생성되었을 때 함수가 완료될 때 삭제 합니다.

---

### Global JavaScript Variables

### 자바스크립트 전역 변수

A variable declared outside a function, becomes GLOBAL.  
A global variable has global scope: All scripts and functions on a web page can access it. 

함수 밖에서 선언되어 지면 전역 변수라고 불립니다.  
전역 변수는 전체 범위를 가집니다: 전체 웹 페이지의 스크립트와 함수에 접근 할 수 있습니다.

<pre class="prettyprint">
Example
var carName = " Volvo";

// code here can use carName

function myFunction() {

    // code here can use	carName 

}
</pre>

---

### Automatically Global

### 전역 자동화

If you assign a value to a variable that has not been declared, it will automatically become a GLOBAL variable.   
This code example will declare carName as a global variable, even if it is executed inside a function.

만약 당신이 변수를 선언하지 않고 값을 할당할 경우에 그것은 전역으로 자동화가 될 것입니다.  
이 예제 코드는 함수 안에서 실행 되더라도 전역 변수carName으로 선언 될 것 입니다.

<pre class="prettyprint">
Example
// code here can use carName

function myFunction() {
    carName = "Volvo";

    // code here can use carName

}
</pre>

---

### The Lifetime of JavaScript Variables

### 자바스크립트 변수의 수명

The lifetime of a JavaScript variable starts when it is declared.  
Local variables are deleted when the function is completed.  
Global variables are deleted when you close the page.

자바스크립트 변수를 선언할 때 수명이 시작 됩니다.  
지역 변수는 함수가 완료 될 때 삭제 됩니다.  
전역 변수는 당신의 페이지를 닫을 때 삭제 됩니다.

---

### Function Arguments

### 함수의 인수

Function arguments (parameters) work as local variables inside functions.

함수의 인수(파라미터)는 함수 안에서 지역 변수로 실행 합니다.

---

### Global Variables in HTML

### HTML안에 전역변수

With JavaScript, the global scope is the complete JavaScript environment.  
In HTML, the global scope is the window object: All global variables belong to the window object.

자바스크립트와 같이 전역 범위에 자바스크립트 환경이 완료 됩니다.  
HTML에서 윈도우 객체의 전역 범위: 모든 전역 변수는 윈도우 객체에 속합니다. 

<pre class="prettyprint">
Example
// code here can use window.carName

function myFunction() {
    carName = "Volvo";
}
</pre>

---

### Did You Know?

### 당신은 알고 있나요?

Your global variables (or functions) can overwrite window variables (or functions).   
Any function, including the window object, can overwrite your global variables and functions.

당신의 전역 변수(또는 함수)는 윈도우 변수(또는 함수)로도 중복하여 사용이 가능합니다.  
윈도우 객체를 포함한 함수는 당신의 전역 변수와 함수를 중복하여 사용할 수 있습니다.

---

---

# JavaScript Events

# 자바스크립트 이벤트

---

HTML events are "things" that happen to HTML elements.  
When JavaScript is used in HTML pages, JavaScript can "react" on these events.

HTMl이벤트는 HTML요소에서 일어나게 됩니다.  
HTML페이지에서 자바스크립트를 사용할 때, 자바스크립트는 그것에 대한 일이 일어나게 됩니다.

---

### HTML Events

### HTML 이벤트

An HTML event can be something the browser does, or something a user does. 
Here are some examples of HTML events:

HTML이벤트는 어떤 브라우저 에서 일어나거나, 사용자에 의해서 일어나게 됩니다.  
여기에 HTML이벤트에 대한 약간의 에제가 있습니다:

* An HTML web page has finished loading
* An HTML input field was changed
* An HTML button was clicked

* HTML 웹 페이지의 로드가 완료
* HTML 필드 입력 변경
* HTML 버튼을 클릭

Often, when events happen, you may want to do something.  
JavaScript lets you execute code when events are detected.  
HTML allows event handler attributes, with JavaScript code, to be added to HTML elements.

종종 당신은 많은 이벤트 들을 하기를 원합니다.  
자바스크립트 이벤트를 감지하여 코드를 실행 할 수 있습니다.  
HTML이벤트 핸들러가 있는 HTML요소를 자바스크립트 코드에 추가합니다.

<pre class="prettyprint">
With single quotes: 따옴표
&lt;some-HTML-element some-event='some JavaScript'&gt;

With double quotes: 쌍따옴표
&lt;some-HTML-element some-event="some JavaScript"&gt;
</pre>

In the following example, an onclick attribute (with code), is added to a button element:

다음 예제에서는 클릭 속성을 엘리먼트 버튼에 추가하는 것 입니다.

<pre class="prettyprint">
Example
&lt;button onclick='getElementById("demo").innerHTML=Date()'&gt;The time is?&lt;/button&gt;
</pre>

In the example above, the JavaScript code changes the content of the element with id="demo".  
In the next example, the code changes the content of its own element (using this.innerHTML):

위의 예제에서는 자바스크립트 코드에서 id="demo"와 요소를 바꾸는 것 이였습니다.  
다음 예제 코드는 자신의 요소를(this.innerHTML을 사용하여)내용을 바꿉니다.

<pre class="prettyprint">
Example
&lt;button onclick="this.innerHTML=Date()"&gt;The time is?&lt;/button&gt;
</pre>

JavaScript code is often several lines long. It is more common to see event attributes calling functions:



<pre class="prettyprint">
Example
&lt;button onclick="displayDate()"&gt;The time is?&lt;/button&gt;
</pre>

---

### Common HTML Events

### 일반적인 HTML이벤트

Here is a list of some common HTML events:

여기에 일반적인 HTML이벤트에대한 목록이 있습니다:

<pre class="prettyprint">
Event			Description
onchange		An HTML element has been changed
onclick			The user clicks an HTML element
onmouseover		The user moves the mouse over an HTML element
onmouseout		The user moves the mouse away from an HTML element
onkeydown		The user pushes a keyboard key
onload			The browser has finished loading the page

이벤트 			설명
onchange 		HTML요소가 변경됩니다.  
onclick 		사용자의 HTML요소를 클릭하면 
onmouseover 		사용자가 요소위에 마우스를 이동시키면
onmouseout 		사용자가 요소에서 다른곳으로 마우스를 이동시키면  
onkeydown 		사용자가 키보드를 누르면
onload 			브라우저 페이지 로딩이 끝나면

</pre>

The list is much longer: [W3Schools JavaScript Reference HTML DOM Events.](http://www.w3schools.com/jsref/dom_obj_event.asp)

이목록 보다 더많은 내용: [W3Schools JavaScript Reference HTML DOM Events.](http://www.w3schools.com/jsref/dom_obj_event.asp)

---

### What can JavaScript Do?

### 자바스크립트는 무슨일을 할 수 있나요?

Event handlers can be used to handle, and verify, user input, user actions, and browser actions:

이벤트 헨들러는 입력, 동작, 브라우저 동작을 하는데 사용 할 수 있습니다.

* Things that should be done every time a page loads
* Things that should be done when the page is closed
* Action that should be performed when a user clicks a button
* Content that should be verified when a user inputs data
* And more ...

* 페이지 로드가 일어날 때마다 실행됩니다.
* 페이지를 닫을 때마다 실행됩니다. 
* 사용자가 버튼을 클릭 할 때 실행 됩니다.
* 사용자가 입력한 데이터내용을 확인 할 때 실행 됩니다.  
* 그리고 더 많이...


Many different methods can be used to let JavaScript work with events:

많은 다른 방법으로 이벤트와 자바스크립트 작업을 할 수 있습니다.

* HTML event attributes can execute JavaScript code directly
* HTML event attributes can call JavaScript functions
* You can assign your own event handler functions to HTML elements
* You can prevent events from being sent or being handled
* And more ...

* HTML이벤트 속성에서 직접 자바스크립트 코드를 실행 할 수 있습니다.
* HTML이벤트 속성은 자바스크립트 함수를 호출 할 수 있습니다.
* 당신은 HTML요소로 자신의 이벤트 핸들러 기능을 할당 할 수 있습니다
* 당신은 전송되는 처리 이벤트를 방지 할 수 있습니다.
* 그리고 더 많이...

You will learn a lot more about events and event handlers in the HTML DOM chapters.

당신은 HTML DOM장에서 더많은 이벤트와 이벤트 핸들러에 대해서 배우게 될 것 입니다.

---

### Test Yourself with Exercises!

### 스스로 연습문제 시험!

[[연습문제1](http://www.w3schools.com/js/exercise.asp?filename=exercise_events1)]
[[연습문제2](http://www.w3schools.com/js/exercise.asp?filename=exercise_events2)]
[[연습문제3](http://www.w3schools.com/js/exercise.asp?filename=exercise_events3)]

---

---

# JavaScript Strings

# 자바스크립트 문자열

---

JavaScript strings are used for storing and manipulating text.

자바스크립트 문자열은 text를 저장하거나 처리할 때 사용합니다.

---

### JavaScript Strings

### 자바스크립트 문자열

A JavaScript string simply stores a series of characters like "John Doe".  
A string can be any text inside quotes. You can use single or double quotes:

자바스크립트 문자열은 "John Doe"와 비슷하게 문자로 저장합니다.  
문자열은 당신의 작은 따옴표나 큰 따옴표 부호안에다가 텍스트를 넣어서 사용할 수 있습니다.

<pre class="prettyprint">
Example
var carname = "Volvo XC60";
var carname = 'Volvo XC60';
</pre>

You can use quotes inside a string, as long as they don't match the quotes surrounding the string:

문자열을 둘러싼 따옴표와 다른 종류의 따옴표를 문자열 안에서 사용할 수 있습니다.

<pre class="prettyprint">
Example
var answer = "It's alright";
var answer = "He is called 'Johnny'";
var answer = 'He is called "Johnny"';
</pre>

---

### String Length

### 문자열 길이

The length of a string is found in the built in property length:

문자열의 길이는 속성의 길이 안에서 만들어진 것중에 찾는다.

<pre class="prettyprint">
Example
var txt = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
var sln = txt.length;
</pre>

---

### Special Characters

### 특수문자

Because strings must be written within quotes, JavaScript will misunderstand this string:

문자열은 따옴표안에서 써야하기 때문에 자바스크립트는 이 문자열을 오해합니다.

<pre class="prettyprint">
var y = "We are the so-called "Vikings" from the north."
</pre>

The string will be chopped to "We are the so-called ".   
The solution to avoid this problem, is to use the \ escape character.  
The backslash escape character turns special characters into string characters:

문자열을 "We are the so-called "로 개조 해야합니다.  
이것의 해결방법은 \를 사용해서 문자를 확장시켜서 문제를 방지해야 합니다. 
역슬래시는 문자는 문자열안에서의 특수문자를 되돌려줍니다.

<pre class="prettyprint">
Example
var x = 'It\'s alright';
var y = "We are the so-called \"Vikings\" from the north."
</pre>

The escape character (\) can also be used to insert other special characters in a string.   
This is the list of special characters that can be added to a text string with the backslash sign:

이스케이프 문자(\)는 문자열에 다른 특수문자를 넣을 수 있습니다.  
역슬래시 기호에 문자를 쓰면 문자열에 추가할 수 있는 특수 문자의 목록 입니다.

<pre class="prettyprint">
Code	Outputs
\'	single quote
\"	double quote
\\	backslash
\n	new line
\r	carriage return
\t	tab
\b	backspace
\f	form feed
</pre>

### Breaking Long Code Lines

### 긴코드의 줄바꿈

For best readability, programmers often like to avoid code lines longer than 80 characters.   
If a JavaScript statement does not fit on one line, the best place to break it is after an operator:

최고의 가독성을 위해서 프로그래머는 흔히 80문자보다 긴 코드를 피해야 합니다.  
자바스크립트문장에서 한줄에 다 표시할 수 없을 경우에 줄을 바꾸기 위한 최고의 장소는 연산자 입니다. 

<pre class="prettyprint">
Example
document.getElementById("demo").innerHTML =
"Hello Dolly.";
</pre>

You can also break up a code line within a text string with a single backslash:

당신은 코드 라인을 text문자열 안에서 \로 라인을 분리할 수 있습니다.

<pre class="prettyprint">
Example
document.getElementById("demo").innerHTML = "Hello \
Dolly!";
</pre>

The \ method is not a ECMAScript (JavaScript) standard.  
Some browsers do not allow spaces behind the \ character. 

\방법은 스크립트 표준 방법이 아닙니다.  
일부의 브라우저에서는 \문자 뒤에 공백을 허용하지 않습니다.

The safest (but a little slower) way to break a long string is to use string addition:

가장 안정적인 긴 문장에서의 줄바꿈은 문자열을 추가하여 줄바꿈 하는 방법입니다.

<pre class="prettyprint">
Example
document.getElementById("demo").innerHTML = "Hello" + 
"Dolly!";
</pre>

You cannot break up a code line with a backslash:

당신은 백슬래시 코드로도 문장을 분리 할 수 있습니다.

<pre class="prettyprint">
Example
document.getElementById("demo").innerHTML = \ 
"Hello Dolly!";
</pre>

### Strings Can be Objects

### 객체로 문자열 사용이 가능합니다

Normally, JavaScript strings are primitive values, created from literals: var firstName = "John"   
But strings can also be defined as objects with the keyword new: var firstName = new String("John")

보통, 자바스크립트 문자열은 상수를 만들때 var firstName = "John"로 만듭니다.  
하지만 문자열은 새로운 객체로 정의하여 만들어 낼 수 도 있습니다.var firstName = new String("John")

<pre class="prettyprint">
Example
var x = "John";
var y = new String("John");

// typeof x will return string 
// typeof y will return object
// x타입은 문자열을 반환한다.
// y타입은 객체를 반환한다.
</pre>

Don't create strings as objects. It slows down execution speed, and produces nasty side effects:

객체와 같은 문자열을 만들면 안됩니다. 그것은 실행속도를 느리게하고, 부작용을 만들어낼 수 있습니다.

When using the == equality operator, equal strings looks equal:

동일한 문자열에 대한 비교를 할때에는 ==평등 연산자를 사용합니다.

<pre class="prettyprint">
Example
var x = "John";             
var y = new String("John");

// (x == y) is true because x and y have equal values
// x와y는 같은 값을 가지고 있기 때문에 true입니다.
</pre>

When using the === equality operator, equal strings are not equal, because the === operator expects equality in both type and value.

=== 연산자를 사용할 경우에는, 문자의 값과 타입까지 비교하기때문에, 두 문자열은 동일하지 않습니다.

<pre class="prettyprint">
Example
var x = "John";             
var y = new String("John");

// (x === y) is false because x and y have different types (string and object)
// (x === y) x와y는 서로다른 문자열 형식을 가지고 있기때문에 false입니다.
</pre>

Or even worse. Objects cannot be compared:

더 나쁜 예로는 객체는 비교할 수 없습니다. 

<pre class="prettyprint">
Example
var x = new String("John");             
var y = new String("John");

// (x == y) is false because x and y are different objects
// (x == x) is true because both are the same object
</pre>

JavaScript objects cannot be compared.

자바스크립트 객체는 비교할 수 없습니다.

---

### String Properties and Methods

### 문자열의 속성과 방법

Primitive values, like "John Doe", cannot have properties or methods (because they are not objects).  
But with JavaScript, methods and properties are also available to primitive values, because JavaScript treats primitive values as objects when executing methods and properties.

기본타입은 속성이나 methods를 가질 수 없습니다.(때문에 그것들은 객체가 아닙니다)  
하지만 자바스크립트는 메서드와 속성을 실행할 때 객체로 기본값을 처리하기 때문에 방법이나 속성을 기본타입으로 사용할 수 있습니다.

String methods are covered in next chapter.

문자열 methods는 다음 장에서 설명합니다.

---

### String Properties

### 문자열 속성

<pre class="prettyprint">
Property	Description
constructor	Returns the function that created the String object's prototype
length	Returns the length of a string
prototype	Allows you to add properties and methods to an object
</pre>

### String Methods

### 문자열 methods

<pre class="prettyprint">
Method			Description
charAt()		Returns the character at the specified index (position)
charCodeAt()		Returns the Unicode of the character at the specified index
concat()		Joins two or more strings, and returns a copy of the joined strings
fromCharCode()		Converts Unicode values to characters
indexOf()		Returns the position of the first found occurrence of a specified value in a string
lastIndexOf()		Returns the position of the last found occurrence of a specified value in a string
localeCompare()		Compares two strings in the current locale
match()			Searches a string for a match against a regular expression, and returns the matches
replace()		Searches a string for a value and returns a new string with the value replaced
search()		Searches a string for a value and returns the position of the match
slice()			Extracts a part of a string and returns a new string
split()			Splits a string into an array of substrings
substr()		Extracts a part of a string from a start position through a number of characters
substring()		Extracts a part of a string between two specified positions
toLocaleLowerCase()	Converts a string to lowercase letters, according to the host's locale
toLocaleUpperCase()	Converts a string to uppercase letters, according to the host's locale
toLowerCase()		Converts a string to lowercase letters
toString()		Returns the value of a String object
toUpperCase()		Converts a string to uppercase letters
trim()			Removes whitespace from both ends of a string
valueOf()		Returns the primitive value of a String object
</pre>

---

### Test Yourself with Exercises!

### 스스로 연습문제 테스트

[[연습문제1](http://www.w3schools.com/js/exercise.asp?filename=exercise_strings1)]
[[연습문제2](http://www.w3schools.com/js/exercise.asp?filename=exercise_strings1)]
[[연습문제3](http://www.w3schools.com/js/exercise.asp?filename=exercise_strings1)]

---

---

# JavaScript String Methods