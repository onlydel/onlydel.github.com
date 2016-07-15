---
layout: page
title: Link Tech
permalink: /linktech/
---

### 맥북 초기설치 프로그램
* [iTerm2](https://www.iterm2.com) 다운로드
* [Git](http://git-scm.com/download/mac) 다운로드 후 설치
* [Xcode dev tools, MAC SDK] `$ git` 명령으로 설치 실행
* [node.js](https://nodejs.org) 다운로드 후 설치
* [Meteor](https://meteor.com) `$ curl https://install.meteor.com/ | sh`
* [Sublime Text](https://www.sublimetext.com)
* [Atom](https://atom.io) 다운로드 후 설치
    - minimap, minimap-find. , minimap-git-diff package
* [Chrome](https://www.google.com/chrome/) 다운로드 후 설치
* [Google Drive](https://tools.google.com/dlpage/drive/index.html) 다운로드 후 설치
* App Store에서 설치
    - Keynote
    - Numbers
    - Pages
    - iBooks Author
    - Xcode
    - KakaoTalk
    - 한컴오피스 뷰어
    - Monosnap
    - Slack
    - popCalendar

### Node.js기반의 간단한 HTTP server
* [http-server](https://github.com/indexzero/http-server)

### HTML, Markdown, PDF Conversions
* [HTML, Markdown을 PDF로 변환하는 방법](http://peterlu.github.io/2014/08/03/markdown_latex_pdf.html)
    - [pandoc](http://pandoc.org) - LaTex가 발목 잡는다.
        + [mactex](https://tug.org/mactex/) - 이걸 다 설치하면 용량이 크고 대신 [BasicTex](http://www.tug.org/mactex/morepackages.html)설치
        + [pdftex - windows](http://tex.stackexchange.com)
    - [wkhtmltopdf](http://wkhtmltopdf.org) - 이걸로 한방에 해결

### 프로토타입 디자인
* [http://facebook.github.io/origami/](http://facebook.github.io/origami/)
* [https://www.google.com/webdesigner/](https://www.google.com/webdesigner/)
* [http://www.relativewave.com/form/](http://www.relativewave.com/form/)
    - 설치

### Blog Framework
* [Hexo](https://hexo.io): Node.js
    - [Tutorial](https://www.sitepoint.com/project-documentation-hexo/)
* [Jekyll](https://jekyllrb.com): Ruby on Rails

### Node hosting
* [http://www.evennode.com](http://www.evennode.com/pricing)
* [호스팅 목록](https://github.com/nodejs/node-v0.x-archive/wiki/Node-Hosting)

### Meteor & MongoDB
* [www.meteor.com](https://github.com/meteor/meteor)
    - [GitHub](https://github.com/meteor/meteor)
* Tutorials
    - 이건 꼭 봐야해 - [Meteorpedia](http://meteorpedia.com/read/Main_Page)
    - [https://github.com/AdamBrodzinski/react-ive-meteor](https://github.com/AdamBrodzinski/react-ive-meteor)
    - [http://javascriptissexy.com/learn-meteor-js-properly/](http://javascriptissexy.com/learn-meteor-js-properly/)
    - [Meteor + Polymer](http://blog.differential.com/meteor-polymer/)
    - [MeteorTips](http://meteortips.com)
* 국제화(internationalize)
    - [i18n](https://atmospherejs.com/tap/i18n)
* Blog
    - [http://mobicon.tistory.com/466](http://mobicon.tistory.com/466)
    - [왜 몽고디비를 쓰면 안되는가?](http://www.sarahmei.com/blog/2013/11/11/why-you-should-never-use-mongodb/)
* Deploy
    - [MUP로 AWS에 배포하기](http://www.curtismlarson.com/blog/2015/11/03/deploy-meteor-to-aws/)
    - [NginX로 멀티 호스팅하기]()
* React for Meteor
    - [http://react-in-meteor.readthedocs.io/en/latest/](http://react-in-meteor.readthedocs.io/en/latest/)

### ATOM
* [code snippet customizing](https://atom.io/docs/latest/using-atom-basic-customization#cson): 메뉴에서 open your snippent메뉴 클릭 또는, 환경설정 package 탭에서 open config folder 클릭, snippets.cson 파일에 추가하면 된다.
    - ${1}, ${2}..는 커서 위치로서 동일한 번호가 여러개인 경우 해당 위치에 동시에 커서가 위치한다.

### AWS
* Nov 01 15: 윈도우 애저는 1년넘게 아직도 계정 가입도 못하고 있는데(결제정보 입력 화면에서 다음으로 넘어가지 않아...), AWS는 약 15분 만에 뚝딱 가입하고 Windows Server 2012인스턴스까지 만들어 로그인까지 성공했다.
  ![](/images/plog/nov0115.png)
* Guide
    - [정적 웹 사이트 호스팅](http://docs.aws.amazon.com/ko_kr/gettingstarted/latest/swh/website-hosting-intro.html)
    - [http://pyrasis.com/](http://pyrasis.com/)
* Sample Codes
    - [Hosting ASP.NET 5 Apps in AWS with DOCKER & CodeDeploy](http://www.slideshare.net/AmazonWebServices/dev302-hosting-aspnet-5-apps-in-aws-with-docker-aws-codedeploy-53675248)
* AWS 온라인 동영상 강의 웨비나
    - [https://aws.amazon.com/ko/blogs/korea/category/webinar/](https://aws.amazon.com/ko/blogs/korea/category/webinar/)

### 핫모듈 대체

### 웹팩(webpack)
* node에서 다른 파일을 include하는 방법으로 require사용. - 이건 웹팩과 별 관계가 없지만...
* [https://github.com/webpack/webpack](https://github.com/webpack/webpack)

### React
* 이거 하나면 다 될거 같은 느낌? [http://getawesomeness.com/get/react#real-apps](http://getawesomeness.com/get/react#real-apps)
* Angular.js의 대안이 될 수 있는가?
* [https://facebook.github.io/react/index.html](https://facebook.github.io/react/index.html)
* React Native를 통해 모바일용 앱을 개발한다. 이 앱은 하이브리드가 아닌 네이티브 앱이다.
* [http://taegon.kim/](http://taegon.kim/)
* [DeView에서 소개](http://serviceapi.rmcnmv.naver.com/flash/outKeyPlayer.nhn?vid=BAA1FFA4240788DDA9D4174FC5C8BA8DCF46&outKey=V1289ef936c3d32277873bd84a5ea14d93e0287a8c7a4eda4905fbd84a5ea14d93e02&controlBarMovable=true&jsCallable=true&skinName=tvcast_white)
* [https://spoqa.github.io/2015/09/09/react-guide-01.html](https://spoqa.github.io/2015/09/09/react-guide-01.html)
* [Flux for React 달걀머리 강좌](https://egghead.io/series/react-flux-architecture-es6?utm_source=drip&utm_medium=email&utm_campaign=what-the-flux&__s=evjzvqvmaquw32ibf8qu)
* 기능
    - [Role based authorization](http://blog.littleblimp.com/post/109540707808/role-based-authorization-with-reactjs)
* React Examples
    - [http://react.rocks/?show=40](http://react.rocks/?show=40)
    - [http://teropa.info/blog/2015/09/10/full-stack-redux-tutorial.html](http://teropa.info/blog/2015/09/10/full-stack-redux-tutorial.html)
    - [http://react.rocks/tag/FullStack](http://react.rocks/tag/FullStack)
    - [http://helmetrex.com](http://helmetrex.com)
* [ReactCheatSheet](http://reactcheatsheet.com) : React 주요 API들을 모아 놓은 건가?
* React Testing
    - [enyme](https://medium.com/airbnb-engineering/enzyme-javascript-testing-utilities-for-react-a417e5e5090f#.vohx7dn37)

### Mac Tip
* Finder에서 hidden folder & file 보기 : defaults write com.apple.finder AppleShowAllFiles YES

  <pre>
    Onlydel-MacBook-Pro:apache2 gotodo$ defaults write com.apple.finder AppleShowAllFiles YES
    Onlydel-MacBook-Pro:apache2 gotodo$ killall Finder
    Onlydel-MacBook-Pro:apache2 gotodo$ defaults write com.apple.finder AppleShowAllFiles NO
    Onlydel-MacBook-Pro:apache2 gotodo$ killall Finder
  </pre>
* [생산성 향상을 위한 터미널 명령어 10개](http://code.tutsplus.com/articles/10-terminal-commands-that-will-boost-your-productivity--net-14105)
* [Custom Shell Prompt](http://itsmetommy.com/2011/02/09/changing-your-shell-prompt/)
    - prompt path변경 `$ nano ~/.profile` 파일에 아래 설정 추가

        <pre>
        # h is the host name, w is the complete path
        export PS1="mac-pro:$ "</pre>

### Node.js
* Setup
    - [http://makerlog.org/posts/js-development-environment/](http://makerlog.org/posts/js-development-environment/)
* Examples
    - [http://www.codemag.com/article/1210041](http://www.codemag.com/article/1210041)
    - [http://okdevtv.com/md/index.html#nodejs/nodejs.md](http://okdevtv.com/md/index.html#nodejs/nodejs.md)

### Maven
* Java Build Tool
* [Maven Book : Maven by Example](http://books.sonatype.com/mvnex-book/reference/index.html)
* [MKyong's Blog](http://www.mkyong.com/maven/)
* Eclipse를 사용할 수도 있겠지만 설치하면서부터 나타나는 오류를 감당하기 힘들어서 Console + SublimeText3으로 간다.
* HSQL
    - [Hyper SQL](http://hsqldb.org) : HSQLDB - 100% Java Database 라고 광고한다.
    - OpenSource RDBMS, java 개발시 테스트용 DB로 주로 사용
    - [설치방법](http://vinant.blogspot.kr/2012/08/setup-hsqldb-on-mac.html)
    - maven에서는 이렇게??    
        <pre class="prettyprint">
        $ mvn hibernate3:hbm2ddl</pre>
        하면... 안되는데?
        + [ERROR] Failed to execute goal org.codehaus.mojo:hibernate3-maven-plugin:2.1:hbm2ddl (default-cli) on project simple-webapp: Could not get ConfigurationTask. -> [Help 1]
        + 해결: hibernate3-maven-plugin 버전을 2.1이 아닌 2.2로 수정    
            <pre class="prettyprint">
            &lt;groupId&gt;org.codehaus.mojo&lt;/groupId&gt;
            &lt;artifactId&gt;hibernate3-maven-plugin&lt;/artifactId&gt;
            &lt;!-- insted of 2.1 as documented inside the Maven by example guide --&gt;
            &lt;version&gt;2.2&lt;/version&gt;  
            ....  </pre>

### Javascript
* OpenSource Libraries
    - [PDF Make](https://github.com/bpampuch/pdfmake)
* 튜토리얼
    - [http://javascript.info](http://javascript.info): 볼만한 내용이 많다. 메모리릭
* ECMAScript2015(ES6)
    - [ECMA Compatibility table](http://kangax.github.io/compat-table/es6/)
    - [BOOK: Exploring ES6](http://exploringjs.com/)
    - [ES6 CheatSheet](https://github.com/DrkSephy/es6-cheatsheet/blob/master/README_ko.md)
    - [Three dots 관련 상세 설명](http://rainsoft.io/how-three-dots-changed-javascript/)
* Front-End(프론트앤드)개발
    - [http://www.slideshare.net/jinkwonlee52?utm_campaign=profiletracking&utm_medium=sssite&utm_source=ssslideview](http://www.slideshare.net/jinkwonlee52?utm_campaign=profiletracking&utm_medium=sssite&utm_source=ssslideview)
* [Javascript Library design tutorial](http://code.tutsplus.com/tutorials/build-your-first-javascript-library--net-26796)
* [MDN](https://developer.mozilla.org/ko/)
    - [객체지향 자바스크립트](https://developer.mozilla.org/ko/docs/Web/JavaScript/Introduction_to_Object-Oriented_JavaScript)
    - 문서
        + [Reference](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference)
    - [클로져](https://developer.mozilla.org/ko/docs/Web/JavaScript/Guide/Closures)
        아래 두 함수가 어떤 차이가 있는지 설명 할 수 있겠는가?

        <pre class="prettyprint">
        function MyObject(name, message) {
          this.name = name.toString();
          this.message = message.toString();
          this.getName = function() {
            return this.name;
          };

          this.getMessage = function() {
            return this.message;
          };
        }

        function MyObject(name, message) {
          this.name = name.toString();
          this.message = message.toString();
        }
        MyObject.prototype = {
          getName: function() {
            return this.name;
          },
          getMessage: function() {
            return this.message;
          }
        };
        </pre>

    - [클로져를 활용한 모듈패턴 이해](http://blog.javarouka.me/2012/02/javascripts-pattern-2-module-pattern.html)
    - [모듈패턴 또다른 이해](http://leejiheg.tistory.com/24)

### 스위프트(Swift)
* [The Swift Programming Language](https://developer.apple.com/swift/resources/)
* [(한글)The ft Programming Language 한글 번역](http://swift.leantra.kr/)
* [Using Swift with Cocoa and Objective-C](https://developer.apple.com/library/ios/documentation/Swift/Conceptual/BuildingCocoaApps/)
* [OBJC(유료)](http://www.objc.io/)
* [NSHipster](http://nshipster.com/)
* [(한글)OSXDEV 커뮤니티](http://www.osxdev.org/forum/index.php)
* [(한글)Swift Korea 페이스북 그룹](https://www.facebook.com/groups/swiftkor/)
* [(한글)스위프트 랩 커뮤니티](http://swiftlab.kr/)
* [(한글)맥부기](http://cafe.naver.com/mcbugi)
* [스탠포드 대학 강의 Developing iOS 8 Apps with Swift](http://itunes.apple.com/kr/course/developing-ios-8-apps-swift/id961180099)
* [Raywenderlich](http://www.raywenderlich.com/)
* [(한글/iOS 개발자)야곰님의 블로그](http://blog.yagom.net/)
* [(한글/iOS 개발자)김근영 개발자 블로그](http://meetkei.com/)
* [(한글)스위프트 페이스북 그룹](https://www.facebook.com/groups/iOSandSwift/)

### GitHub
* 암호나 민감한 파일은 public 저장소에서 어떻게 관리 하면 좋을까?
    - [http://stackoverflow.com/questions/2397822/what-is-the-best-practice-for-dealing-with-passwords-in-github](http://stackoverflow.com/questions/2397822/what-is-the-best-practice-for-dealing-with-passwords-in-github)

### 개발자 아카데미, 실력테스트, 코드 테스트
* [CodeAcademy](http://www.codecademy.com/)
* [lavida](http://lavida.us)
* [spoj](http://www.spoj.com)
* [온라인 코드 컴파일 테스트](http://ideone.com)

### 읽을거리
* 리모트 근무 환경에 대해(디지털 노마드)
    - 한국 디지털 노마드 선구자?: [도유진](http://dareyourself.net){:target="_blank"}
    - 비석세스의 디노마드 관련 기사: [beSeccuss](http://besuccess.com/author/doyoujin/){:target="_blank"}
    - 디노마드의 핵심은 역시 원격근무: [http://spoqa.github.io/2014/08/03/remote.html](http://spoqa.github.io/2014/08/03/remote.html){:target="_blank"}
    - 스마트 워크: [http://www.bloter.net/archives/229923](http://www.bloter.net/archives/229923){:target="_blank"}
* [올바른 띄어쓰기 규칙 “자신의 호흡에 맞게”](http://ppss.kr/archives/24576){:target="_blank"}
* [바지 벗고 일하면 안되나요?](http://www.aladin.co.kr/shop/wproduct.aspx?ISBN=8994506985&ttbkey=ttboutsideris1727002&COPYPaper=1)

### 소프트웨어 리뷰 / 리서치 사이트
* 이런 사이트를 어떻게 받아들여야 할까? 수익모델이 뭘까 궁굼해 지기도 하고, 국내에도 이런 사이트가 존재하는지도 궁금하다.
* [http://www.capterra.com/help-desk-software/#infographic](http://www.capterra.com/help-desk-software/#infographic)
* [http://www.tekrevue.com/tip/reorder-spotlight-search-results/](http://www.tekrevue.com/tip/reorder-spotlight-search-results/)

### 웹사이트 템플릿 Template , 테마 Theme
* [https://almsaeedstudio.com/](https://almsaeedstudio.com/)
* [https://wrapbootstrap.com/](https://wrapbootstrap.com/)

### Visual Studio
* [Visual Studio Code & 2015 소개글](http://blogs.msdn.com/b/eva/archive/2015/05/08/visual-studio-2015.aspx)

### Visual Studio Code (Mac)
* Settings
    - 줄바꿈 컬럼(0이면 자동줄바꿈): "editor.wrappingColumn": 0
    - 행 번호: "editor.lineNumbers": true

### 소프트웨어 기술
* [도커](http://navercast.naver.com/contents.nhn?rid=122&rid=&contents_id=66402)
* [OCP - Open Container Project](http://www.opencontainers.org/)


### IoT
* [ms-iot GitHub](https://github.com/ms-iot)
* 비콘 (Beacon)
    * [ETRI 비콘 연구실](http://beacon.smartcontent.kr/introduce)
    * [대박 Dron Apps Gall.](http://flyver.co/drone-apps/)
* 인텔
    * [인텔 IoT 홈](https://software.intel.com/en-us/iot/home)
* Arduino
    * [http://www.arduino.cc/en/Guide/HomePage](http://www.arduino.cc/en/Guide/HomePage)
    * [아두이노 콥터](http://copter.ardupilot.com/)
    * [아두이노 카페 강좌 pdf](http://cafe.naver.com/CafeMemberNetworkView.nhn?m=view&clubid=17467872&memberid=hgycap#)
    * [위 강좌쓴 사람의 카페](http://cafe.naver.com/sketchurimagination)
    * [MPU카페](http://cafe.naver.com/mpucafe)
    * [아두이노 블루투스 통신 카페](http://cafe.naver.com/convergencekorea)
    * [핀잇](https://www.pinterest.com/pin/416864509234161587/)
    * [아두이노 콥터](http://blog.naver.com/sb1214/30183380948)
    * [Real Story](http://hs36.tistory.com/)
    * 온라인 강좌
        * [http://wiki.vctec.co.kr/opensource/arduino](http://wiki.vctec.co.kr/opensource/arduino)
        * [하드카피 월드](http://www.hardcopyworld.com/)
        * [끄으적끄으적](http://blog.daum.net/seongju4645/6)
        * [빵판닷컴](http://bbangpan.tistory.com)
    * 필요한 기본 부품
        * [MPU 스타터 키트: 15,500 + 2,600](http://cafe.naver.com/mpucafe/4821)
        * [아두이노 우노 호환보드 + 적외선거리센서: 20,000 + 2,500](http://www.gmarket.co.kr/pay/Basket.asp)
        * [아트로봇](http://artrobot.co.kr/)
        * 부품판매
            * http://www.eleparts.co.kr/main/main.php
            * http://www.ic114.com/ajaxwww/theme/001/default.aspx
            * [디바이스마트](http://www.devicemart.co.kr/)
            * [디바이스마트 블로그](http://www.ntrexgo.com/)
            * http://www.funnykit.co.kr/shop/main/index.php
            * http://www.robot.co.kr/front/php/category.php?cate_no=24
            * http://e홈메이드클럽.com/

### ASP.NET
* [docs.asp.net](http://docs.asp.net)
* [Repository, Unit of Work Pattern](http://www.asp.net/mvc/overview/older-versions/getting-started-with-ef-5-using-mvc-4/implementing-the-repository-and-unit-of-work-patterns-in-an-asp-net-mvc-application)
    * [Unit of Work](http://aspnetboilerplate.com/Pages/Documents/Unit-Of-Work)
* EntityFramework
    - [기본](http://www.asp.net/mvc/overview/getting-started/getting-started-with-ef-using-mvc/creating-an-entity-framework-data-model-for-an-asp-net-mvc-application)
    - [복잡](http://www.asp.net/mvc/overview/getting-started/getting-started-with-ef-using-mvc/creating-a-more-complex-data-model-for-an-asp-net-mvc-application)
    - [관계데이터 가져오기](http://www.asp.net/mvc/overview/getting-started/getting-started-with-ef-using-mvc/reading-related-data-with-the-entity-framework-in-an-asp-net-mvc-application)
* iTextSharp
    - [Open Source PDF Library](https://github.com/itext/itextsharp/releases) - not free
* Angula.js
    - [CookBook: samples](https://github.com/Wintellect/Angular-MVC-Cookbook)
    - [codecademy online learn](http://www.codecademy.com/learn/learn-angularjs)
* Session
    - `eng`[Session in ASP.NET 5](http://www.exceptionnotfound.net/session-in-asp-net-5/)
* ASP.NET + Angula.js + MongoDB
    - [Goolge Search](https://www.google.co.kr/search?q=asp.net+entity+framework+mongodb&oq=asp.net+entity+framework+mongodb&aqs=chrome..69i57.9087j0j7&sourceid=chrome&es_sm=91&ie=UTF-8#newwindow=1&q=asp+net+web+api+mongodb)
    - [blog article](http://blogs.msdn.com/b/henrikn/archive/2012/02/19/using-web-api-with-mongodb.aspx)
    - [MongoDB c# API](http://api.mongodb.org/csharp/)
    - [CodePlex sample](http://aspnet.codeplex.com/sourcecontrol/latest#Samples/WebApi/MongoSample/ReadMe.txt)
    - [GitHub sample](https://github.com/jacqinthebox/AddressBook/tree/master/AddressBook)

### Developing hybrid mobile apps
* [Apache Cordova™](https://cordova.apache.org)
* [Ionic](http://ionicframework.com/)

### SaaS with Azure
* [Windows Azure IaaS vs. PaaS vs. SaaS](http://robertgreiner.com/2014/03/windows-azure-iaas-paas-saas-overview/)
* [Building SaaS products with Windows Azure](http://www.slideshare.net/8KMiles/building-saas-products-with-windows-azure)
* [Building SaaS Applications on Windows AZURE](http://www.davidchappell.com/writing/white_papers/Building_SaaS_Apps_on_Windows_Azure-Chappell_v1_0.pdf)
* [Building Highly Scalable and Available SaaS Applications with Azure SQL Database](http://channel9.msdn.com/Events/Build/2015/2-678)
* Multi-Tentant
    * [https://msdn.microsoft.com/en-us/library/ff966499.aspx](https://msdn.microsoft.com/en-us/library/ff966499.aspx)

### 맥에서 자바개발
* [http://mirwebma.tistory.com/27](http://mirwebma.tistory.com/27)
* [http://devist.tistory.com/97](http://devist.tistory.com/97)
* [맥에서 개발용 웹서버 구축 가이드](https://mallinson.ca/osx-web-development/) : 다른 어떤것 보다 이게 제일 완벽함.(virtualhost)
    - 여기에 추가로 custom port를 쓰려면 : httpd.conf에서

      <pre class="prettyprint">
      Listen 80
      <mark>Listen 8080 <-- 추가</mark>
      ....
      ServerName localhost:80
      <mark>ServerName localhost:8080 <-- 추가</mark>
      </pre>
* 클라우드 서버 구축
    - [PaaS Cloud](https://www.openshift.com/products)
    - [MongoDB](https://mongolab.com)

### 개발자 블로그, 커뮤니티
* [http://leastprivilege.com](http://leastprivilege.com)
* [https://justhackem.wordpress.com/](https://justhackem.wordpress.com/)
* [이상한모임](http://blog.weirdx.io/)
* [http://blog.outsider.ne.kr/](http://blog.outsider.ne.kr/)
* [dogfeet](http://dogfeet.github.io/)
* [정보시각화 스터디](http://infovis.kr)
* [https://github.com/pismute](https://github.com/pismute)
* [김태곤 javascript](http://taegon.kim)
* [naver D2](http://d2.naver.com/)
* 자비스크립트
    - [Nonblock](http://blog.javarouka.me)
    - [지똥이](http://leejiheg.tistory.com)

### 소프트웨어 디자인
* [UML Diagram](http://www.uml-diagrams.org/){:target="_blank"}
* [Star UML](http://staruml.io/){:target="_blank"}
* [UML Example - ASP.NET](http://www.mandanemedia.com/archives/917)

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
