---
layout: post
title: MVC를 이용해 RealGrid에 데이터를 표현하기
date: 2015-03-24 21:13:31 +9:00 GMT
categories: 
  - ASP.NET
  - draft
tags: 
  - ASP.NET
  - MVC
  - RealGrid
---

### 들어가며
MVC를 이용해 RealGrid에 데이터를 표현하기 위해 유사한 개념의 표현방식을 참조해 보자.
mvc에서 jQuery Datatables를 통합한 포스트를 참조해 본다.

http://www.codeproject.com/Articles/155422/jQuery-DataTables-and-ASP-NET-MVC-Integration-Part

내용을 보면 황당하리 만치 별게 없다.

백앤드에서는 MVC를 이용해 Json형식의 데이터를 돌려주는 Controller를 만든다.

프론트앤드에서는 Javascript를 이용해 Datatables에 Ajax를 통해 Controller의 method를 호출 하는 것으로 마무리 된다. 실제 구체적인 코드는 환경에 따라 조금 달라질 수 있을지 몰라도 RealGrid도 마찬가지방법으로 처리가 가능할 것으로 보인다.

그렇다면 사실 프론트앤드에서는 WEB API냐 MVC Library이냐를 고민할 필요가 없는 것이다. 즉, MVC 구조의 Service를 만들고 최종 Controller단계에서 WEB API와 MVC Controller로 구분해 주면 되는 것 아닌가? 하지만, 확실 하지는 않다. 좀 더 정확한 실험을 하고 진행 해야 한다.

---
**참조**

* [http://www.codeproject.com/Articles/155422/jQuery-DataTables-and-ASP-NET-MVC-Integration-Part](http://www.codeproject.com/Articles/155422/jQuery-DataTables-and-ASP-NET-MVC-Integration-Part){:target="_blank"}