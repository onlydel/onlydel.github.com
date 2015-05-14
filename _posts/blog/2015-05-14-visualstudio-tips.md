---
layout: post
title: Visual Studio 코딩 도우미(Coding Aids)
date:   2015-05-14 21:13:31 +9:00 GMT
categories: 
  - Visual Studio
  - tip
tags: 
  - Visual Studio
  - Coding Aids
  - 코딩도우미
---

### 들어가며
Visual Studio의 Coding Aids에 대해 정리해 봅니다.  
Visual Studio에는 코드를 생성하거나 변경할때 도움을 받을 수 있는 도우미 기능들이 많이 있습니다. 대부분 코딩시 에디터에서 어떤식으로든 알려주기 때문에 알고 있는 것들도 있지만 숨어 있는 기능도 많은 것 같아 발견할 때 마다 조금씩 정리해 보겠습니다.

#### 코드스니핏(Code Snippet)
코드스니핏은 예약어를 입력한 다음 `tab`키를 클릭하면 코드를 완성 시켜주는 기능 입니다. VB, C#언어에 따라 다르며, 개발자가 직접 원하는 스니펫을 만들어 사용할 수도 있습니다.

* `prop`   
  프로퍼티 코드라인이 자동으로 생성됩니다.

  <pre class="prettyprint">
  // prop입력 후 tab키
  public int MyProperty { get; set; }</pre>


#### 인텔리센스(IntelliSense)

* Implement Abstract Base Class   
  Interface나 Abstract Calss를 상속 받는 새로운 클래스를 구현 할때 필요한 method들을 자동으로 생성해 주는 인텔리센스 입니다.