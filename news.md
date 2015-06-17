---
layout: page
title: News
permalink: /news/
---

### June 2015
* 9, [Visual Studio Code v0.3.0 업데이트](https://code.visualstudio.com/updates){:target="_blank"}
    한글 관련 버그들이 아직도 약간 남아 있지만 입력은 가능합니다.

### May 2015
* 18, 어처구니 없는 사건 발생
* 2, [**Visual Studio 2015 RC 버전 발표**](http://blogs.msdn.com/b/visualstudio/archive/2015/04/29/build-2015-news-visual-studio-code-visual-studio-2015-rc-team-foundation-server-2015-rc-visual-studio-2013-update-5.aspx){:target="_blank"}   
    4월 29일자로 Visual Studio 2015 RC 버전이 발표되었습니다. 기존 VS버전 중 Premium, Ultimate사용자는 Enterprise로 무상 업그레이드 할 수 있는 프로모션도 진행한다고 합니다.   
    에디션은 Community, Professional, Enterprise로 구분되어 있으며 [제품 비교 사이트](https://www.visualstudio.com/products/compare-visual-studio-2015-products-vs){:target="_blank"}에서 기능을 비교할 수 있습니다. 제품 평가를 위해 [다운로드 페이지](https://www.visualstudio.com/en-us/downloads/visual-studio-2015-downloads-vs){:target="_blank"}에서 Community와 Enterprise버전을 다운받을 수 있습니다.  
    더불어 [Visual Studio 2013 Update 5 RC](https://www.visualstudio.com/news/vs2013-update5-vs?CR_CC=200626821){:target="_blank"}버전도 발표되었습니다.
* 2, [**Visual Studio Code 발표**](https://code.visualstudio.com/){:target="_blank"}   
    Visual Studio Code라는 이름의 개발자용 편집기가 Build 2015를 통해 발표되었습니다. 단순 편집기라기보다는 개발도구입니다. 크로스플랫폼(Linux, Mac OSX, and Windows) 동작이 가능한 Code는 ASP.NET 5 등 클라우드 애플리케이션 빌드, 디버깅이 가능하다고 합니다. 현재 0.1.0버전인데 한글입력에 문제가 있어 메일로 문의하니 인코딩 이슈가 있다는 답변 입니다.   
    자체 Git 호환기능이 포함되어 있어 개인적으로 무척 기대하고 있습니다.

### April 2015
* 29, [**Build 2015 컨퍼런스**](http://www.buildwindows.com/){:target="_blank"}   
    4월 29일 ~ 5월 1일까지 사흘간 센프란시스코에서 Build 2015행사가 개최되었습니다. 행사에 대한 키노트는 Korea Evangelist 블로그에 정리된 내용이 있습니다.    
    [Build 2015 Day1 KeyNote 요약](http://blogs.msdn.com/b/eva/archive/2015/04/30/build-2015-day-1-keynote.aspx){:target="_blank"}    
    [Build 2015 Day2 KeyNote 요약](http://blogs.msdn.com/b/eva/archive/2015/05/02/build-2015-day-2-keynote.aspx){:target="_blank"}    
    세계 투어도 진행하고 있습니다. 우리나라는 6월 1일 코엑스에서 개최됩니다. 참가신청은 [여기](https://seoul.build15.com/){:target="_blank"}서...

* 8, [**ASP.NET Identity 2.2.1 릴리즈**](http://blogs.msdn.com/b/webdev/archive/2015/04/07/asp-net-identity-2-2-1.aspx){:target="_blank"}   
    2015년 2월 20일 공개된 2.2.0버전에서 리포트된 버그들을 수정했다고 합니다. ASP.NET Identity는 ASP.NET 응용프로그램에서 사용할 수 있는 사용자관리 시스템으로 EF(Entity Framework), Core, OWIN 이라는 패키지로 구분되어 있으며, EF패키지와 OWIN패키지는 Core에 의존적이므로 Core를 먼저 설치해야 합니다.   
        Install-Package [Microsoft.AspNet.Identity.EntityFramework](https://www.nuget.org/packages/Microsoft.AspNet.Identity.EntityFramework){:target="_blank"} –Version 2.2.1   
        Install-Package [Microsoft.AspNet.Identity.Core](https://www.nuget.org/packages/Microsoft.AspNet.Identity.Core){:target="_blank"} -Version 2.2.1   
        Install-Package [Microsoft.AspNet.Identity.OWIN](https://www.nuget.org/packages/Microsoft.AspNet.Identity.OWIN){:target="_blank"} -Version 2.2.1   
    2.0에서 마이그레이션은 데이터베이스 스키마 변경없이 가능 하다고 합니다.

* 6, [**Visual Studio Tools for Unity 2.0 Preview 2 릴리즈**](http://blogs.msdn.com/b/visualstudio/archive/2015/04/06/visual-studio-tools-for-unity-2-0-preview-2.aspx){:target="_blank"}   
    Visual Studio Tools for Unity(VSTU) 2.0 Preview 2가 릴리즈 되었다는 소식 입니다.   
    VSTU는 Visual Studio에서 Unity 게임 툴과 플렛폼으로하는 작업을 지원하는 애드온 툴입니다. 이번 Preview 2의 주요 기능은 지난달 업그레이드된 Unity 5를 공식적으로 지원하는 것입니다. VSTU는 아래 링크를 통해 Visual Studio 갤러리에서 다운로드 받을 수 있습니다.

* 1, [**Visual Studio 2015 제품 라인업**](http://blogs.msdn.com/b/visualstudio/archive/2015/03/31/announcing-the-visual-studio-2015-product-line.aspx){:target="_blank"}   
    Visual Studio 2015 제품 라인업이 발표되었습니다. 기존 제품군에 있던 Visual Studio Professional 2013 with MSDN과 Visual Studio Ultimate 2013 with MSDN이 Visual Studio Enterprise 2015 with MSDN으로 통합되었습니다.  
    그외의 제품군은 동일한 에디션을 유지하게 되는것 같습니다. Express버전도 계속 제공될 것이라고 합니다.   
    최종 제품 출시는 올 2015년 여름쯤이 될것 같습니다. 이미 사용자 프리뷰를 위해 CTP버전이 배포되고 있으니 조금 일찍 Visual Studio 2015를 접해보고 싶은 개발자 분들은 [VS2015 CTP 6 Download](http://visualstudio.com/en-us/downloads/visual-studio-2015-ctp-vs){:target="_blank"}에서 다운로드 받을 수 있습니다.    
    4월 1일 가격도 공개가 되었습니다. [Visual Studio 2015 Product Editions](https://www.visualstudio.com/products/vs-2015-product-editions){:target="_blank"} 사이트에서 확인 가능합니다. 이전 버전 사용자에 대한 한시적 무료 업그레이드도 해준다고 합니다. 이런걸 왜 한시적으로 하는지 이해 할 수 없지만 말입니다.(마케팅이 모에요~~?)   
    개인적으로 이런저런 에디션을 구분하고 가격을 별도로 책정하는 모습이 마음에 들지는 않습니다. 그냥 딱 애플처럼만 하면 좋을 것 같다는 생각입니다. OS는 딱 하나의 에디션만, 개발툴은 무료로, 말입니다. 물론 이런 생각 = 짧은 생각 이란것 인정하지만, 불가능한 것만은 아니라고 생각합니다. 길게보면 지금도 예전보다는 많이 나아진 모습이긴 합니다.   
    Visual Studio가 Windows를 구입한 모든 사용자에게 무료로 공개되는 날이 하루 빨리 찾아왔으면 하는 바램입니다.

### March 2015
* 18, [**MSBuild 엔진 깃허브에 오픈소스로 공개**](http://blogs.msdn.com/b/dotnet/archive/2015/03/18/msbuild-engine-is-now-open-source-on-github.aspx){:target="_blank"}    
    MSBuild엔진도 [깃허브](https://github.com/Microsoft/msbuild){:target="_blank"}에 공개되었다는 소식입니다. ASP.NET을 비롯한 MS의 주요 개발 기술들도 이미 MS에서 운영하는 [코드플렉스](http://aspnetwebstack.codeplex.com/){:target="_blank"}에 오픈소스로 공개된 이 후, 깃허브로 2015년 3월 18일 이전한 상태 입니다.

### February 2015
* 23, [**Visual Studio 2015 CTP 6**](https://www.visualstudio.com/news/vs2015-vs#uidbugxaml){:target="_blank"}    
    Visual Studio 2015 CTP 6가 2월 23일 배포되었습니다.[VS2015 CTP 6 Download](http://visualstudio.com/en-us/downloads/visual-studio-2015-ctp-vs){:target="_blank"}