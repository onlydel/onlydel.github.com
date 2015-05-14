---
layout: page
title: About
permalink: /about/
---

### jekyll
* 베트남 개발자 지킬관련 블로그 포스팅: [Vietnam, Trần Xuân Trường blog](https://truongtx.me){:target="_blank"}
* 아주 상세한 지킬 튜토리얼: [Tutorial](https://www.andrewmunsell.com/tutorials/jekyll-by-example){:target="_blank"}
* 리퀴드 언어에 대한 문서: [liquid Document](https://docs.shopify.com/themes/liquid-documentation/filters/array-filters){:target="_blank"}
* 공백을 포함한 태그나 카테고리를 입력하는 방법: 아래와 같이 메타정보를 입력한다.
        
        ---
        layout: post
        title: Visual Studio Code for Mac
        date:   2015-05-11 12:55:58 +9:00 GMT
        categories: 
          * Visual Studio
        tags: 
          * Visual Studio Code
          * VS
          * VisualStudio
        ---
* 지킬에서 사이드메뉴 나 포스팅 내에 `ul` tag내에 있는 문자열로 목록을 필터링 하는 방법: [관련포스팅](/another code/2015/05/09/깃허브-지킬에서-사이드메뉴-필터링.html)
* `post_url` <mark>사용시 오류 발생.(이것 때문에 엄청 고생했다.)</mark>
* 목록에서 `pre` tag를 사용하는 방법: `pre` tag를 문단의 맨 앞 컬럼에서 시작할 경우 목록을 벗어나게 된다. 이 경우 `pre` tag 부분을 모두 선택한 다음 `tab`키를 눌러 앞쪽에 `tab`문자 하나를 넣어 주면 된다.
    
    <pre class="prettyprint">
    1. 하나
    2. 둘
        &lt;pre class=&quot;prettyprint&quot;&gt;
        &lt;/pre&gt;</pre>

* 목록에서 `pre` tag로 코드를 처리 하지 않고 `네개의 공백`으로 코드를 처리할 경우는 두 개의 `tab`문자를 넣어 주면 된다.
* 마크다운 포스트를 작성하면서 html로 변환될때 html tag에 특정 attribute를 삽입하는 방법: 아래 두 코드를 비교해 보면 알 수 있다.

    `[링크](http://link/)`

    <pre class="prettyprint">
    &lt;a href=&quot;http://link/&quot;&gt;&#xb9c1;&#xd06c;&lt;/a&gt;</pre>

    `[링크](http://link/){:target="_blank"}`

    <pre class="prettyprint">
    &lt;a href=&quot;http://link/&quot; target=&quot;_blank&quot;&gt;&#xb9c1;&#xd06c;&lt;/a&gt;</pre>

### GitHub
* 암호나 민감한 파일은 public 저장소에서 어떻게 관리 하면 좋을까?
    - [http://stackoverflow.com/questions/2397822/what-is-the-best-practice-for-dealing-with-passwords-in-github](http://stackoverflow.com/questions/2397822/what-is-the-best-practice-for-dealing-with-passwords-in-github)

### 읽을거리
* 리모트 근무 환경에 대해(디지털 노마드)
    - 한국 디지털 노마드 선구자?: [도유진](http://dareyourself.net)
    - 비석세스의 디노마드 관련 기사: [beSeccuss](http://besuccess.com/author/doyoujin/)
    - 디노마드의 핵심은 역시 원격근무: [http://spoqa.github.io/2014/08/03/remote.html](http://spoqa.github.io/2014/08/03/remote.html)

### 읽고 싶은 책
* [바지 벗고 일하면 안되나요?](http://www.aladin.co.kr/shop/wproduct.aspx?ISBN=8994506985&ttbkey=ttboutsideris1727002&COPYPaper=1)

### 웹사이트 템플릿 Template , 테마 Theme
* [https://almsaeedstudio.com/](https://almsaeedstudio.com/)
* [https://wrapbootstrap.com/](https://wrapbootstrap.com/)

### Visual Studio
* [Visual Studio Code & 2015 소개글](http://blogs.msdn.com/b/eva/archive/2015/05/08/visual-studio-2015.aspx)

### IoT
* [ms-iot GitHub](https://github.com/ms-iot)
* Aduino
    * [http://www.arduino.cc/en/Guide/HomePage](http://www.arduino.cc/en/Guide/HomePage)

### ASP.NET
* [docs.asp.net](http://docs.asp.net)
* EntityFramework
    - [기본](http://www.asp.net/mvc/overview/getting-started/getting-started-with-ef-using-mvc/creating-an-entity-framework-data-model-for-an-asp-net-mvc-application)
    - [복잡](http://www.asp.net/mvc/overview/getting-started/getting-started-with-ef-using-mvc/creating-a-more-complex-data-model-for-an-asp-net-mvc-application)
    - [관계데이터 가져오기](http://www.asp.net/mvc/overview/getting-started/getting-started-with-ef-using-mvc/reading-related-data-with-the-entity-framework-in-an-asp-net-mvc-application)

### .NET 블로거
* [http://leastprivilege.com](http://leastprivilege.com)

