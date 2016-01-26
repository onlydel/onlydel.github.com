---
layout: post
title: react를 위한 webpack정리 (I)
date:   2015-12-28 22:24:23 +9:00 GMT
categories: 
  - Javascript
tags: 
  - javascript
  - webpack
  - reactjs
  - react
  - browserify
  - 웹팩
  - 리액트
---

## init

Webpack React로 개발해보고자 [react webpack cookbook](https://christianalfoni.github.io/react-webpack-cookbook/) 보면서 정리해 본다. 기회가 되면 정식 번역이라도... 하고 싶지만 내 영어실력에 번역은 원작자를 욕먹이는 일이 될 수도 있다.

## webpack 기본

"webpack이 뭔가?" 부터 설명할 수는 없다. 왜냐하면 나도 그 질문에 명확한 해답을 가지고 있지 않기 때문. [webpack 사이트](https://webpack.github.io/)에는 module bundler라고 정의 되어있다. 묶음이나 꾸러미를 의미하는 bundle의 의미로 보면 `모듈들을 묶어주는 놈` 이 되겠다.

javascript를 모듈화 하려는 노력은 세계적인 추세이고 모듈화라는건 하면 할 수록, 명확하지만 복잡해지는 것 같다. 어려워진다고 해야 하나?

webpack은 browserify의 기능을 포함한 빌드툴 같으면서 걸프나 그런트같은 빌드툴과도 혼합해서 사용할수 있는 것을 보면 좀더 포괄적인 기능을 내포하고 있는 것 같다.


#### 일단, 설치

설치는 글로벌로 먼저 해주고,

<pre>
~/$ npm install webpack -g
</pre>

#### 프로젝트

지금 연습을 위해 만들 프로젝트는 index.js라는 javascript파일을 import한 index.html 페이지를 브라우저에서 실행 하는 것이고 화면에는 h1 테그를 사용한 "Hello, World"이란 문구의 헤더 텍스트가 표시되도록 하는 것이다.

프로젝트를 위해 폴더를 만들고 초기화 및 webpack(개발용)을 설치한다.

<pre>
~/$ mkdir ~/Sites/webpack-sample
~/$ cd ~/Sites/webpack-sample
webpack-sample/$ npm init
...
webpack-sample/$ npm install webpack --save--dev
</pre>

#### package.js

npm init에 의해 node module package config파일이 생성된다. npm init시 입력했던 내용이 config에 포함되고 build, start등 npm의 명령을 수행할 script를 정의할 수 있는 파일이다.

npm package.js파일은 아래에서 설명을 좀더 추가 한다.

#### webpack.config.js

webpack을 실행하기 위해 환경설정 파일이 필요하다. 환경설정 파일은 webpack.config.js로 만들어 준다. 연습 프로젝트를 위한 설정파일은 아래와 같이 구성해 준다.

*webpack.config.js*
<pre class="prettyprint">
var path = require('path');

module.exports = {
    entry: path.resolve(__dirname, 'app/main.js'),
    output: {
        path: path.resolve(__dirname, 'www'),
        filename: 'index.js',
    },
};
</pre>

위 파일을 풀어서 설명하면 "app/main.js파일을 빌드해서 www폴더에 index.js라는 이름으로 모듈패키지파일을 만들어라!" 정도가 되지 않을까?

여기까지 하면 프로젝트 폴더는 아래와 같은 구조가 된다. 

<pre>
.
├── node_modules
├── package.json
└── webpack.config.js
</pre>

#### 웹 프로젝트 구성

연습 프로젝트를 좀더 발전시켜보자. 

우선 요구사항을 반영하기 위해 "Hello, World" 텍스트를 h1 태그로 랜더링하기 위한 요소(element)생성하는 컴포넌트를 만들자. 이 컴포넌트는 app폴더에 component.js파일에 만든다.

*app/component.js*
<pre class="prettyprint">
'use strict'

module.exports = function() {
  var el = document.createElement('h1');
  if (el) {
    el.innerHTML = "Hello World";
  }
  return el;
}
</pre>

'use strict'를 쓰면 javascript문법을 좀더 엄격하게 적용하여 빌드하게 된다. 엄격한 코드 규칙이 디버깅에 더 좋다. 

위에서 만든 컴포넌트를 페이지의 `app` id를 가진 div태그의 child로 넣어 주는 main.js 모듈을 만든다.

*app/main.js*
<pre class="prettyprint">
'use strict';

var component = require('./component.js');

document.getElementById('app').appendChild(component());
</pre>

메인페이지는 www폴더에 index.html파일로 구성한다.

*www/index.html*
<pre class="prettyprint">
&lt;!DOCTYPE html&gt;
&lt;html&gt;
  &lt;head&gt;
    &lt;meta charset=&quot;utf-8&quot;&gt;
    &lt;title&gt;webpack test&lt;/title&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;div id=&quot;app&quot;&gt;&lt;/div&gt;
    &lt;script src=&quot;index.js&quot;&gt;&lt;/script&gt;
  &lt;/body&gt;
&lt;/html&gt;
</pre>

여기까지 하면 디렉토리 구조는 아래와 같다.

<pre>
.
├── app
│   ├── component.js
│   └── main.js
├── www
│   └── index.html
├── node_modules
├── package.json
└── webpack.config.js
</pre>

#### 빌드

webpack으로 빌드를 해보자. 그냥 webpack.config.js파일이 있는 폴더에서 webpack만 실행 하면 된다.

<pre>
webpack-sample/$ <mark>webpack</mark>
Hash: 57c4209c4176b4da3342
Version: webpack 1.12.9
Time: 45ms
   Asset     Size  Chunks             Chunk Names
index.js  1.74 kB       0  [emitted]  main
   [0] ./app/main.js 116 bytes {0} [built]
   [1] ./app/component.js 150 bytes {0} [built]
</pre>

빌드하면 www폴더에 index.js파일이 생성되는 것을 볼 수 있다.

#### npm build

npm 명령을 사용해서 module을 빌드하거나 웹 서버를 시작(start) 하기 위해 package.js파일의 `scripts` 속성을 이용한다.

우선 npm 명령뒤에 빌딩 스템을 숨기기 위해서 프로젝트내에 webpack을 따로 설치해 준다. `--save`옵션으로 package.js파일에 dependency정보를 기록하고 개발전용으로 하고 싶으면 `--save--dev`옵션을 사용한다.

<pre>
webpack-sample/$ npm install webpack --save--dev
</pre>

*package.js*
<pre class="prettyprint">
{
  "name": "webpack-sample",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    <mark>"build": "webpack",</mark>
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC",
  "dependencies": {
    "webpack": "^1.12.9"
  }
}
</pre>

마킹 부분을 추가해 주면 아래와 같이 `npm build`명령으로 `webpack`의 빌드 스크립트를 실행 할 수 있다. 연습 프로젝트에서는 단순하기 때문에 굳이 써야할 이유를 물을수도 있겠지만 다양한 옵션들을 사용하거나 빌딩 스텝을 자동화 하기 위해서 복잡한 명령들을 단순화 할 수 있는 npm명령을 사용하기로 한다. 타이핑을 취미로 하고 싶다면 말릴 이유는 없지만...

아래 명령을 실행하면 `webpack`명령을 실행한 것과 동일하게 index.js가 빌드된다. `npm build`명령도 동일.

<pre>
webpack-sample/$ npm run build
</pre>

결과를 웹서버에서 열어보면 아래처럼...

![](/images/blog/20151228-javascript-webpack-for-react.png)

## webpack-dev-server

개발시 자동 웹브라우징 기능까지 제공해 주는 도구로, webpack-dev-server를 이용하면 훨씬 효과적으로 개발 할 수 있다. 프로젝트 폴더에서 npm 으로 설치한다.

<pre>
webpack-sample/$ npm install webpack-dev-server --save
</pre>

설치하고 package.js에 `dev` 스크립트를 추가하자.

*package.js*
<pre class="prettyprint">
{
  ...
  "scripts": {
    "build": "webpack",
    "dev": "webpack-dev-server --devtool eval --progress --colors --hot --content-base www"
  }
  ...
}
</pre>

`npm run dev`를 실행 하면 해당 스크립트가 실행된다.

`webpack-dev-server`를 실행하면 웹서버가 실행되며 경로는 `http://localhost:8080/`이 된다. 포트 정보를 수정 하려면 webpack.config.js 모듈에 아래 속성을 추가/수정 한다.

<pre>
devServer: {
  inline: true,
  port: 3333
}
</pre>

`webpack-dev-server`의 옵션에 대해 좀더 알아보면...

1. `--devtool eval` 디버깅을 위해 devtool을 선택한다. 참조: [--devtool](http://webpack.github.io/docs/configuration.html#devtool)
2. `--progress` 빌드 하는 동안 progress를 보여준다.
3. `--color` 터미널에 빌드정보가 컬러플하게 보여준다.
4. `--hot` [hot module replacement](http://webpack.github.io/docs/webpack-dev-server.html#hot-module-replacement)
5. `--content-base www` www폴더를 출력 폴더로 지정하고 웹서버의 접근 경로도 해당 폴더가 최상위 경로가 된다.

## 브라우저 자동갱신

`webpack-dev-server`는 실행시 프로젝트 폴더의 파일 변화를 감시한다. 파일이 변경되면 브라우저를 자동으로 갱신한다. 이 과정에서 프로젝트를 다시 빌드하고 변화를 서버에 알려 브라우저를 갱신하도록 한다. 

실험을 위해 www폴더 밑에 있는 index.html파일의 내용을 수정하고 저장해보자. 또, 변동될때 마다 애플리케이션을 리플래시 할 필요가 있는 파일들은 configuration의 entry point에 추가해 주면 된다.

여기서는 index.html파일을 직접 만들었는데 단순 테스트를 위해 기본적인 index.html파일을 자동으로 생성해주는 툴도 있다. [html-webpack-plugin](https://www.npmjs.com/package/html-webpack-plugin)을 참고하자.

## 파일 require하기

모듈 시스템에서 `require`는 현재 모듈에서 또 다른 모듈을 필요로 하여 불러온다는 의미로 이해하자. 보통 다른 언어에서 import나 using, uses등과 같은 의미로 해석하면 되겠다.

webpack은 현존하는 모듈 패턴들. 즉, ES6 Modules, CommonJs, AMD 패턴을 모두 사용할 수 있다. 이런 패턴들은 알고보면 거기서 거기, 그놈이 그놈... 동일한 방법으로 작동된다. 참고페이지에 있는 예를 적어보면 아래와 같다. 

나는 최근 개인적으로 es6 패턴을 사용하는데, 온라인에 있는 많은 코드들은 CommonJs로 되어 있다. 또, 여러패턴이 혼용되기도 한다. 이 부분은 좀 신기하기도 하지만 생각해 보면 당연하고 간혹 나 조차도 그렇게 쓸때가 있다.    
어쨋거나 AMD 패턴은 이제 거의 사용하지 않는 것 같고 최근 올라오는 글들을 보면 대부분 CommonJs나 ES6로 되어 있는것 같고, ES6의 비율이 점점더 높아지는 추세인듯 하다. 

이 글에서는 가능한한 ES6만 사용해서 코드를 작성하기로 한다.


패턴별로 모듈을 로드하는 코드의 예는 아래와 같다.

#### ES6 modules
<pre class="prettyprint">
import MyModule from './MyModule.js';
</pre>

#### CommonJs
<pre class="prettyprint">
var MyModule = require('./MyModule.js');
</pre>

#### AMD
<pre class="prettyprint">
define(['./MyModule.js'], function (MyModule) {

});
</pre>

## 경로(path) 이해하기

모듈은 파일 경로로 로드한다. 다음과 같은 파일구조가 있다고 가정하면,

* /app
  * /modules
    * MyModule.js
  * main.js (entry point)
  * utils.js

entry point인 main.js에서 /app/modules/MyModule.js파일을 불러오기(require)위해 코드를 작성해 보면 아래처럼 코딩한다.

<pre class="prettyprint">
// ES6
import MyModule from './modules/MyModule.js';
</pre>

여기서 `./`는 일반적인 파일시스템 처럼 현재파일의 경로를 의미하며 상위 경로는 `../`를 사용한다.

그럼 MyModule.js파일에서 utils.js파일을 불러오는 코드를 작성해 보자.

<pre class="prettyprint">
// ES6
import MyModule from './../util.js';

import MyModule from '/util.js';
</pre>

첫 번째 줄은 위에서 설명했고, 두 번째 줄은 utils.js가 최상위 경로, 즉 root경로에 있기 때문에 `/`를 사용해도 된다. 이런 두 가지 경로 표현 방법을 일반적으로 상대경로(relative path)와 절대경로(absolute path)라고 할 수 있다. 절대경로의 기준이 되는 점(entry point)는 configuration에서 설정한 entry file의 위치일 것이다. 위의 파일구조에서 main.js파일이 있는 지점이 root가 되겠다.

## 파일 확장명

Webpack에 의해서 bundle될때에는 .js나 .jsx, css등 파일확장명은 없애도 된다. 하지만 이것은 node_modules에 설치된 모듈명을 require하는 것과는 전혀 다른 의미 이므로 구분해서 이해해야 한다.


모든 설명을 한 페이지에 다 넣으려고 했는데 좀 지루한것 같아. 파일을 나누기로 한다.
본격적인 react에 대한 내용은 [(II)](/javascript/2016/01/08/javascript-webpack-for-react2.html)에 이어서 한다.

---
**참조**

* [react webpack cookbook](https://christianalfoni.github.io/react-webpack-cookbook/){:target="_blank"}
