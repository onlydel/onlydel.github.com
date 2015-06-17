---
layout: post
title: Hello, RealGridJS!
date:   2015-03-30 21:13:31 +9:00 GMT
categories: 
  - RealGrid
tags: 
  - RealGridJS
  - RealGrid
  - Setup
---

<script type="text/javascript" src="/script/dlgrids_eval.js"></script>
<script type="text/javascript" src="/script/realgridjs.js"></script>

<script>
$(document).ready( function() {

    var gridView;
    var dataProvider;
    
    RealGridJS.setTrace(false);
    RealGridJS.setRootContext("/script");
    
    dataProvider = new RealGridJS.LocalDataProvider();
    gridView = new RealGridJS.GridView("realgrid");
    gridView.setDataSource(dataProvider);
   
});
</script>

### 들어가며

이 글의 목적은 RealGridJS를 웹 화면에 표시해 보는 것입니다. 실제로 해보면 이 과정은 그리 어려운게 아니라는 것을 알 수 있습니다. 단순히 RealGridJS가 올라갈 `<div>`태그를 결정하고 간단한 스크립트코드만 작성해 주면 됩니다.

### 설치에 필요한 파일

그럼 이제 RealGrid를 개발 환경에 맞게 설치해 보겠습니다. 만약, RealGrid가 없다면 [평가판요청](http://www.realgrid.com/#download){:target="_blank"}페이지에서 평가판을 요청하면 메일로 평가판을 받을 수 있습니다. 메일에 포함된 RealGrid파일중 설치에 <mark>반드시 필요한 파일</mark>은 아래 두 개의 javascript파일들과 RealGridJS화면 구성에 필요한 assets폴더 입니다.

***참고로 RealGridJS는 JQuery와 같은 외부 라이브러리가 필요없습니다.***

        /dlgrids_eval.js
        /realgridjs.js
        /assets/


### 코드작성
이제 RealGridJS를 웹 화면에 올려 보겠습니다.   

1. 두 개의 스크립트파일을 순서대로 include합니다. 반드시 `dlgrigs_eval.js`파일이 먼저 와야 합니다.

    <pre class="prettyprint">
&lt;script type=&quot;text/javascript&quot; src=&quot;/script/dlgrids_eval.js&quot;&gt;&lt;/script&gt;
&lt;script type=&quot;text/javascript&quot; src=&quot;/script/realgridjs.js&quot;&gt;&lt;/script&gt;</pre>

2. GridView객체를 저장할 gridView변수를 정의 합니다.

    <pre class="prettyprint">
    var gridView;</pre>

3. LocalDataProvider객체를 저장할 dataProvider변수를 정의 합니다.

    <pre class="prettyprint">
    var dataProvider;</pre>

4. assets폴더의 위치를 변경하기 위해 setRootContext(path)함수를 호출 합니다. 이때 `assets`이라는 <mark>폴더 이름은 변경할 수 없습니다.</mark> 반드시 path에 지정된 경로 아래에 `assets`이라는 이름의 폴더가 존재해야 하며, 그 아래에 화면을 구성하기 위한 이미지 파일들이 있어야 합니다.

    <pre class="prettyprint">
    RealGridJS.setRootContext(&quot;/script&quot;);</pre>

5. LocalDataProvider와 GridView객체를 생성하고 GridView의 DataSource를 생성된 LocalDataProvider로 지정하는 코드를 추가 합니다.

    <pre class="prettyprint">
    dataProvider = new RealGridJS.LocalDataProvider();
    gridView = new RealGridJS.GridView(&quot;realgrid&quot;);
    gridView.setDataSource(dataProvider);</pre>

6. RealGridJS가 표시될 `div` 태그를 작성하고 크기를 지정해야 합니다. <mark>크기가 지정되지 않으면 화면에 RealGridJS가 표시되지 않습니다.</mark>

    <pre class="prettyprint">
    &lt;div id=&quot;realgrid&quot; style=&quot;width: 100%; height: 200px;&quot;&gt;&lt;/div&gt;</pre>


### 전체코드 (Gist)

{% gist onlydel/f0c3a94199bbb3c412a4 %}

### Hello, RealGrid!

<div id="realgrid" style="width: 100%; height: 200px;"></div>


---
**참조**

* [RealGrid Help](http://help.realgrid.com){:target="_blank"}