---
layout: post
title: Hello, RealGridJS!
date:   2015-03-30 21:13:31 +9:00 GMT
categories: 
  - RealGrid
  - draft
  - setup
tags: 
  - RealGridJS
  - RealGrid
---

<script type="text/javascript" src="/script/jszip.min.js"></script>
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

이 글의 목적은 RealGridJS를 웹 화면에 표시해 보는 것입니다. 실제로 해 보니 이 과정은 그리 어려운게 아니었습니다. 단순히 RealGridJS가 올라갈 `<div>`태그를 결정하고 간단한 스크립트코드만 작성해 주면 끝납니다.

### 설치에 필요한 파일

### js파일, assets폴더

assets폴더 위치 변경: RealGridJS.setRootContext();

### 라이선싱

### Code 
이제 RealGrid를 웹 화면에 올려 보겠습니다.

<pre class="prettyprint">
&lt;script&gt;
$(document).ready( function() {
    var gridView;
    var dataProvider;
    
    RealGridJS.setTrace(false);
    RealGridJS.setRootContext(&quot;/script&quot;);
    
    dataProvider = new RealGridJS.LocalDataProvider();
    gridView = new RealGridJS.GridView(&quot;realgrid&quot;);
    gridView.setDataSource(dataProvider);
});
&lt;/script&gt;

&lt;div id=&quot;realgrid&quot; style=&quot;width: 100%; height: 200px;&quot;&gt;&lt;/div&gt;
</pre>



### Hello, RealGrid!

<div id="realgrid" style="width: 100%; height: 200px;"></div>


---
**참조**

* [RealGrid Help](http://help.realgrid.com){:target="_blank"}