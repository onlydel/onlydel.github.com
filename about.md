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
    - 스마트 워크: [http://www.bloter.net/archives/229923](http://www.bloter.net/archives/229923)

### 읽고 싶은 책
* [바지 벗고 일하면 안되나요?](http://www.aladin.co.kr/shop/wproduct.aspx?ISBN=8994506985&ttbkey=ttboutsideris1727002&COPYPaper=1)

### 웹사이트 템플릿 Template , 테마 Theme
* [https://almsaeedstudio.com/](https://almsaeedstudio.com/)
* [https://wrapbootstrap.com/](https://wrapbootstrap.com/)

### Visual Studio
* [Visual Studio Code & 2015 소개글](http://blogs.msdn.com/b/eva/archive/2015/05/08/visual-studio-2015.aspx)

### Visual Studio Code (Mac)
* Settings
    - 줄바꿈 컬럼(0이면 자동줄바꿈): "editor.wrappingColumn": 0
    - 행 번호: "editor.lineNumbers": true
    
### IoT
* [ms-iot GitHub](https://github.com/ms-iot)
* Arduino
    * [http://www.arduino.cc/en/Guide/HomePage](http://www.arduino.cc/en/Guide/HomePage)
    * [아두이노 콥터](http://copter.ardupilot.com/)
    * [아두이노 카페 강좌 pdf](http://cafe.naver.com/CafeMemberNetworkView.nhn?m=view&clubid=17467872&memberid=hgycap#)
    * [위 강좌쓴 사람의 카페](http://cafe.naver.com/sketchurimagination)
    * [MPU카페](http://cafe.naver.com/mpucafe)
    * [아두이노 블루투스 통신 카페](http://cafe.naver.com/convergencekorea)
    * 필요한 기본 부품
        * [MPU 스타터 키트: 15,500 + 2,600](http://cafe.naver.com/mpucafe/4821)
        * [아두이노 우노 호환보드 + 적외선거리센서: 20,000 + 2,500](http://www.gmarket.co.kr/pay/Basket.asp)

### ASP.NET
* [docs.asp.net](http://docs.asp.net)
* EntityFramework
    - [기본](http://www.asp.net/mvc/overview/getting-started/getting-started-with-ef-using-mvc/creating-an-entity-framework-data-model-for-an-asp-net-mvc-application)
    - [복잡](http://www.asp.net/mvc/overview/getting-started/getting-started-with-ef-using-mvc/creating-a-more-complex-data-model-for-an-asp-net-mvc-application)
    - [관계데이터 가져오기](http://www.asp.net/mvc/overview/getting-started/getting-started-with-ef-using-mvc/reading-related-data-with-the-entity-framework-in-an-asp-net-mvc-application)
* iTextSharp
    - [Open Source PDF Library](https://github.com/itext/itextsharp/releases) - not free

### Front-End Development
* [CodeAcademy](http://www.codecademy.com/)

### Developing hybrid mobile apps
* [Apache Cordova™](https://cordova.apache.org)
* [Ionic](http://ionicframework.com/)

### SaaS with Azure
* [Windows Azure IaaS vs. PaaS vs. SaaS](http://robertgreiner.com/2014/03/windows-azure-iaas-paas-saas-overview/)
* [Building SaaS products with Windows Azure](http://www.slideshare.net/8KMiles/building-saas-products-with-windows-azure)
* [Building SaaS Applications on Windows AZURE](http://www.davidchappell.com/writing/white_papers/Building_SaaS_Apps_on_Windows_Azure-Chappell_v1_0.pdf)
* [Building Highly Scalable and Available SaaS Applications with Azure SQL Database](http://channel9.msdn.com/Events/Build/2015/2-678)

### 블로그
* [http://leastprivilege.com](http://leastprivilege.com)
* [https://justhackem.wordpress.com/](https://justhackem.wordpress.com/)
* [이상한모임](http://blog.weirdx.io/)
* [http://blog.outsider.ne.kr/](http://blog.outsider.ne.kr/)

