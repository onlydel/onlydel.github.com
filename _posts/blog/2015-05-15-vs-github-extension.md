---
layout: post
title: GitHub Extension for Visual Studio
date:   2015-05-15 21:13:31 +9:00 GMT
categories: 
  - Visual Studio
tags: 
  - Visual Studio 2015
  - VS 2015
  - GitHub
  - Extension
---

![](/images/blog/20150515-github-extension-for-vs.png)

### 들어가며

2015년 4월 30일 MS Build 2015가 한참 진행중이던 이때 깃허브(GitHub)에서 Visual Studio 2015(VS 2015)에서 깃허브 연결을 도와줄 도우미 확장팩을 개발/발표했습니다. 정말 극적이라는 생각이 듭니다.  
기존에도 팀 탐색기에 Git 도우미가 있었습니다. 하지만, 깃허브와 연결이 힘들고 사용법도 깃허브에 맞추어져 있지 않아 불편한점이 많았습니다. 그래서 저는 그냥 [윈도우용 깃허브 데스크탑](https://windows.github.com)을 사용하고 있었습니다. 깃허브에서 만든 깃허브 전용 도우미는 얼마나 좋은지 잔뜩 기대하는 마음으로 사용해 보았습니다.

### 설치

설치는 아래 세가지 방법으로 할 수 있습니다.

* VS 2015 RC를 새롭게 설치하는 경우라면 사용자 설치를 선택하여 GitHub Extension for Visual Studio를 선택하면 설치가 됩니다.
* 기존에 설치된 VS 2015에 추가로 설치하려면 TOOLS > Extensions and Updates메뉴를 실행한 다음 Visual Studio online Gallery에서 검색하여 설치 할 수 있습니다.
* 또는, [다운로드 페이지](https://visualstudio.github.com/downloads/GitHub.VisualStudio.vsix)를 통해서 다운로드한 다음 설치 할 수 있습니다.

![](/images/blog/20150515-github-extension-for-vs-01.png)

### 연결

1. 깃허브에 연결하기 위해서 팀 탐색기의 연결관리 아이콘을 눌러 연결관리 페이지로 이동 합니다.

    ![](/images/blog/20150515-github-extension-for-vs-02.png)

2. `연결관리`링크를 클릭하면 `Connect to GitHub` 메뉴가 보입니다. 메뉴를 클릭합니다.
3. 로그인 화면이 표시됩니다. 깃허브 아이디로 로그인 합니다.
4. 팀 탐색기에 깃허브 섹션이 추가됩니다.

    ![](/images/blog/20150515-github-extension-for-vs-03.png)

### 클론(Clone)

1. 팀 탐색기의 깃허브 섹션에서 `Clone`을 클릭합니다.
2. 깃허브의 리파지토리(Repository)목록 화면이 표시됩니다.
3. 클론할 리파지토리를 선택하고 `Clone`버튼을 클릭 합니다.
    
    ![](/images/blog/20150515-github-extension-for-vs-04.png)

4. 팀 탐색기의 `로컬 Git 리포지토리`섹션에 클론한 리파지토리가 표시됩니다.
5. 클론한 리파지토리에서 오른쪽 버튼을 눌러 `열기`를 클릭합니다.
6. 팀 탐색기의 홈 탭이 열리면서 클론한 리파지토리 정보가 표시됩니다.

### 생성(Create)

1. 팀 탐색기의 깃허브 섹션에서 `Create`를 클릭합니다.
2. 깃허브의 리파지토리생성 화면이 표시됩니다.
3. 정보를 입력한 다음 `Create`버튼을 클릭합니다.

    ![](/images/blog/20150515-github-extension-for-vs-05.png)

4. 로컬에 해당 폴더로 가서 리파지토리가 생성된 것을 확인 합니다.
5. 동시에 GitHub에도 리파지토리가 생성된 것을 확인 합니다.

    ![](/images/blog/20150515-github-extension-for-vs-06.png)

### 리파지토리에 VS 2015 솔루션 만들기

1. 팀 탐색기의 홈탭으로 이동 합니다.
2. 위 섹션에서 생성된 리파지토리가 열려있는지 확인하고 솔루션 섹션의 새로 만들기...를 클릭하여 새로운 프로젝트를 생성합니다.

    ![](/images/blog/20150515-github-extension-for-vs-07.png)

3. 새 프로젝트를 생성하면 솔루션 탐색기에 새로 생성된 프로젝트 파일들이 표시됩니다.
4. 솔루션 노드의 컨텍스트 메뉴에서 `커밋`을 클릭합니다.

    ![](/images/blog/20150515-github-extension-for-vs-08.png)

5. 커밋 메시지를 입력하고 커밋 버튼 콤보를 펼쳐 `커밋`, `커밋 후 푸시`, `커밋 후 동기화` 중 선택하여 실행합니다.

    ![](/images/blog/20150515-github-extension-for-vs-09.png)

6. 로컬에만 커밋한 상태라면 동기화 탭으로 이동하여 동기화, 페치, 풀, 푸시등 필요한 작업을 계속 할 수 있습니다.

### 결론

깃허브를 사용한지 오래되지 않았지만, 이제서야 알고 사용하게 된게 안타까울 정도 입니다. 앞으로 MS의 플렛폼 지향 정책에 따라 어찌보면 경쟁사라고도 할 수 있는 깃허브와도 친하게 지내며 너그러운 정책을 펴는 것을 보면 가난한 개발사의 가난한 개발자로서 기분이 뿌듯해 지기도 합니다.   
지금 까지 맥에서는 어느정도 안정적으로 동작되던 깃허브 데스크탑이 윈도우에서는 버그도 있고 불편한 점도 있었습니다. 이제 VS 2015를 이용한 프로젝트인 경우는 좀더 편하게 깃허브를 이용 할 수 있을것 같습니다.
기타 문서파일과 같이 VS의 프로젝트에 포함되지 않는 파일같은 경우는 따로 관리해야 하는 불편함이 있기는 하지만, 그 점을 감안해도 안정적이고 편리해진 확장프로그램임이 분명 합니다. 

---
**참조**    

* [GitHub Extension for Visual Studio](https://visualstudio.github.com){:target="_blank"}
* [GitHub Windows](https://windows.github.com){:target="_blank"}