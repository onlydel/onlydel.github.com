---
layout: post
title: 패러렐즈 Visual Studio Text Editor 스크롤을 부드럽게 하는 방법
date:   2015-03-31 21:13:31 +9:00 GMT
categories: 
  - Visual Studio
  - tip
tags: 
  - 페러렐즈
  - Visual Studio
  - Parallels
---

![](/images/blog/20150331-vs-parallels.jpg)

### 제 개발환경은

OS X가 설치된 맥북 프로 레티나 15 014(late)입니다. 물론 맥에서 Visual Studio를 직접 실행 하는 것은 아닙니다. 페러렐즈 가상환경에 Windows 10 Preview버전을 설치하고 그 위해 Visual Studio Community 2013을 설치하여 개발 하고 있습니다. 외부 입력장치도 마우스나 외장 키보드는 사용하지 않고 맥북의 본체에 붙어 있는 트랙패드를 사용하고 있습니다.

가상환경에서 Visual Studio를 실행하면서 몇 가지 불편한 점들이 있었습니다. 가상환경에서 Visual Studio사용에 대한 보다 자세한 내용은 기회가 되면 따로 정리해 볼 생각입니다. 

Visual Studio의 Text Editor상에서 맥북의 트랙패드를 써서 스크롤을 할 때의 불편했던 점은 맥 OS에서 손가락 끝에 화면이 밀착되어 붙어 있는 듯한 스크롤링의 느낌이 가상 환경으로 들어가면 전혀 다른 이질적인 느낌이 되어 버립니다. 좀더 기술적으로 보면 맥에서는 픽셀단위로 스크롤링이 이루어지기 때문에 한 순간도 스크롤이 끊어지는 느낌이 없습니다. 하지만, 윈도우로 들어가면 행단위로 스크롤링이 되기 때문에 일정 범위내에서의 움직임은 스크롤에 영향을 주지 않게 됩니다. 이 것은 외장 마우스의 휠 기능을 사용할 때에는 오히려 불편함이 없게 느껴지지만, 트랙패드를 사용하는 경우 마치 동작이 중지된 것 같은 기분이 들게 합니다. 

이런 불편함에 대한 해결 방법을 찾던중 같은 문제로 고민을 하던 누군가가 만들어 놓은 Visual Studio의 확장기능을 알게 되었습니다. 이 확장기능을 설치한 다음 마치 맥에서 처럼 부드러운 스크롤이 Text Editor에서 가능해졌습니다. 지원하는 VS버전은 2010, 2012, 2013, 2015라고 합니다. 2013과 2015에서는 작동을 확인했습니다. 2010에서는 안된다는 사람도 있는것 같습니다.

### 어쨌거나

OS X + 맥북 트랙패드 + 패러렐즈(Parallels)가상환경 + Visual Studio를 사용하고 있다면 분명 그 불편한 느낌을 알고 계시리라 믿습니다. 아래 링크의 확장기능을 설치 하시면 편안하게 코딩 하실 수 있을 겁니다.


---
**참조**    

* [https://visualstudiogallery.msdn.microsoft.com/5fcc21b1-2c9b-4768-a5da-e309811d6b9e](https://visualstudiogallery.msdn.microsoft.com/5fcc21b1-2c9b-4768-a5da-e309811d6b9e){:target="_blank"}