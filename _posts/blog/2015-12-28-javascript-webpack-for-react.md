---
layout: post
title: react를 위한 webpack정리
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

[react webpack cookbook](https://christianalfoni.github.io/react-webpack-cookbook/) 보면서 정리하는 것임.

## webpack 기본

"webpack이 뭔가?" 부터 설명할 수는 없다. 왜냐하면 나도 그 질문에 명확한 해답을 가지고 있지 않기 때문. [webpack 사이트](https://webpack.github.io/)에는 module bundler라고 정의 되어있다. 

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

## 파일 require하기

모듈 시스템에서 require는 현재 모듈에서 또 다른 모듈을 필요로 한다는 의미로 이해 하면 될것 같다. 

---
**참조**

* [react webpack cookbook](https://christianalfoni.github.io/react-webpack-cookbook/){:target="_blank"}
