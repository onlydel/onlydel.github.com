---
layout: post
title: jQuery로 iFrame 사용하기
date:   2015-10-21 13:24:23 +9:00 GMT
categories: 
  - Another Code
tags: 
  - html
  - jquery
  - parseHTML
  - iframe
---

문제의 발단은 특정 HTML파일을 가져와서 iFrame에 넣는 작업을 하는 과정에서 발생했다.

## 요구사항
1. 특정 HTML파일에는 jquery등을 이용해 RealGrid가 실행되는 페이지이다.
2. 메인페이지에서 이 HTML파일을 불러와서 iFrame영역에 넣고 페이지에서 실행되는 기능이 실행되어야 한다.
3. 페이지에는 RealGrid, jquery등 javascript파일이 include되어 있지만 파일을 불러오는 시점에 해당 라이브러리의 버전을 선택하여 동적으로 include하기 위해 파일에서는 삭제처리했다.
4. HTML파일은 메인페이지와 동일한 도메인 내에 있으며 ajax get으로 가져온다.

이 문제를 해결하기 위해 여러가지 실험을 했다.

### jquery.parseHTML()

우선 가져온 HTML파일 소스를 파싱하기 위해 jquery.parseHTML()을 사용했다. jquery.parseHTML()은 $(html)로 대신 할 수 있다. 하지만, 문제는 파싱과정에서 html, head, body같은 tag들이 제거된다는 사실을 알게 되었다.(http://api.jquery.com/jquery.parsehtml/) 

<pre class="prettyprint">
$.get(&#039;/testcase/id_50000.html&#039;, function (data) {

$(&quot;#gridFrame&quot;).attr(&quot;src&quot;, &quot;&quot;);

var $html = $(&#039;&lt;html/&gt;&#039;).append(data.replace(/(head|body)/ig, &#039;$1a&#039;));
var $body = $html.find(&#039;bodya&#039;);
var $head = $html.find(&#039;heada&#039;);

$body.append(&quot;&lt;script src=&#039;https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js&#039;&gt;&lt;/script&gt;&quot;);
$body.append(&quot;&lt;script src=&#039;/realgrids/1.0.12.2033-eval/realgridjs-lic.js&#039;/&gt;&quot;);
$body.append(&quot;&lt;script src=&#039;/realgrids/1.0.12.2033-eval/realgridjs_eval.1.0.11.min.js&#039;/&gt;&quot;);
$body.append(&quot;&lt;script src=&#039;/realgrids/1.0.12.2033-eval/realgridjs-api.1.0.11.js&#039;/&gt;&quot;);
$body.append(&quot;&lt;script src=&#039;/realgrids/1.0.12.2033-eval/jszip.min.js&#039;/&gt;&quot;);


var body = $(&quot;&lt;html/&gt;&quot;).append($(&quot;&lt;body/&gt;&quot;).append($body.children())[0]);

console.log(body);


console.log($(&quot;&lt;head/&gt;&quot;).append($head.children())[0]);



})
</pre>

### iFrame에 대한 실험

크롬 브라우저에서 랜더링 되는 형태를 확인 하기 위해 여러가지 방법으로 iFrame에 코드를 넣어 보기로 한다.

1. `$("#gridFrame").attr("src", "");` : 빈값이 들어가게 된다. 원래 있던 값은 지워진다.

    <pre class="prettyprint">
    &lt;iframe id=&quot;gridFrame&quot; allowtransparency=&quot;true&quot; frameborder=&quot;1&quot; src=&quot;&quot;&gt;&lt;/iframe&gt;    </pre>

2. HTML DOM의 document.write()함수를 이용해 직접 코드를 작성 할 수도 있다.

    <pre class="prettyprint">
    > document.getElementById(&quot;gridFrame&quot;).contentWindow.document.write(&quot;&lt;!DOCTYPE html&gt;&quot;</pre>

3. html 파일을 읽어서 넣을 수 있다.

    <pre class="prettyprint">
    $("#gridFrame").attr("src", "/testcase/id50000.html");</pre>

<pre>
//이렇게는 안된다.
$('#gridFrame').append('<!DOCTYPE html>');
$('#gridFrame').contents().append('<!DOCTYPE html>');

//이거는 되긴하지만 경고 있다.
var scripts = [$(&quot;&lt;script src=&#039;/realgrids/1.0.12.2033-eval/realgridjs-lic.js&#039;/&gt;&quot;), $(&quot;&lt;script src=&#039;https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js&#039;/&gt;&quot;)]
$('#gridFrame').contents().find('head').append(scripts);
//경고
Synchronous XMLHttpRequest on the main thread is deprecated because of its detrimental effects to the end user's experience. For more help, check http://xhr.spec.whatwg.org/.

//이것도 마찬가지 노드는 추가되고 경고 있다.
var scripts = [$(&quot;&lt;script src=&#039;/realgrids/1.0.12.2033-eval/realgridjs-lic.js&#039;/&gt;&quot;), $(&quot;&lt;script src=&#039;https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js&#039;/&gt;&quot;)]
$('#gridFrame').contents().find('head').append(scripts);

//이것도 노드는 들어가지만 경고있다.
var scripts = &quot;&lt;script src=&#039;/realgrids/1.0.12.2033-eval/realgridjs-lic.js&#039;/&gt; &lt;script src=&#039;https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js&#039;/&gt;&quot;
$('#gridFrame').contents().find('head').append(scripts);


//최종
$.get(url, function (data) {

  var $html = $(&#039;&lt;html/&gt;&#039;).append(data.replace(/(head|body)/ig, &#039;$1a&#039;));
  var $body = $html.find(&#039;bodya&#039;);
  var $head = $html.find(&#039;heada&#039;);
  var $script = $head.find(&#039;script&#039;);

  $head.find(&#039;script&#039;).remove();

  $body.append(&quot;&lt;script src=&#039;https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js&#039;/&gt;&quot;);
  $body.append(&quot;&lt;script src=&#039;/realgrids/1.0.12.2033-eval/realgridjs-lic.js&#039;/&gt;&quot;);
  $body.append(&quot;&lt;script src=&#039;/realgrids/1.0.12.2033-eval/realgridjs_eval.1.0.11.min.js&#039;/&gt;&quot;);
  $body.append(&quot;&lt;script src=&#039;/realgrids/1.0.12.2033-eval/realgridjs-api.1.0.11.js&#039;/&gt;&quot;);
  $body.append(&quot;&lt;script src=&#039;/realgrids/1.0.12.2033-eval/jszip.min.js&#039;/&gt;&quot;);
  $body.append($(&quot;&lt;script/&gt;&quot;).append(&quot;RealGridJS.setRootContext(&#039;/realgrids/1.0.12.2033-eval&#039;);&quot;));
  $body.append($script);

  var newhtml = $(&quot;&lt;html/&gt;&quot;);
  var body = $(&quot;&lt;body/&gt;&quot;).append($body.children());
  var head = $(&quot;&lt;head/&gt;&quot;).append($head.children());

  newhtml.append([head, body]);

  //console.log(newhtml[0]);

  var result = newhtml[0].innerHTML;
  var iframe = document.getElementById(&#039;gridFrame&#039;);

  if(iframe.contentDocument) doc = iframe.contentDocument;
  else if(iframe.contentWindow) doc = iframe.contentWindow.document;
  else doc = iframe.document;

  doc.open();
  doc.writeln(result);
  doc.close();

});

</pre>

---
**참조**

* [https://github.com/miconblog/Slide/tree/master/20140305](https://github.com/miconblog/Slide/tree/master/20140305){:target="_blank"}
* [http://code.tutsplus.com/tutorials/meeting-grunt-the-build-tool-for-javascript--net-24856](http://code.tutsplus.com/tutorials/meeting-grunt-the-build-tool-for-javascript--net-24856){:target="_blank"}