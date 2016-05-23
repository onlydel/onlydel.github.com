---
layout: post
title: Git! 너 뭐야?
date:   2016-04-03 22:24:23 +9:00 GMT
categories: 
  - Another Code
tags: 
  - 깃
  - 깃허브
  - git
  - github
---

## init

Git은 버전관리, 파일 리비전관리(revision)를 위한 아주 괜찮은 녀석(tool)이다. Git은 분산 버전 관리 시스템(DVCS: Distributed Version Control System) 이다. 전에는 중앙형 버전 관리 시스템(CVCS)인 SVN을 주로 사용했었는데, 회사에서도 이제 git을 사용하고 있다. Git관리를 위해 툴을 사용하는 것도 좋은 방법이지만 가능한한 CLI를 이용하고 싶다. 

이 문서는 기억력이 많이 딸리는 요즘의 나를 위해(ㅠ.ㅠ) 상황(case)별 Git 활용 방법을 정리한다.


## 로컬(local) PC에 새로운 저장소(repository)를 만들어야 한다.

프로젝트의 소스코드 폴더를 Git으로 관리하기 위해 새로운 저장소를 만들려면 `init`명령을 사용한다.

`git init`명령을 실행하여 새로운 리파지터리를 만들고 `git status` 명령으로 상태를 확인한다.
<pre>
$ mkdir premium
$ cd premium
premium/$ git init
Initialized empty Git repository in /Users/onlydel/Sites/premium/.git/

premium/$ git status
On branch master

Initial commit

nothing to commit (create/copy files and use "git add" to track)
</pre>

## 깃허브에 추가된 새로운 저장소를 로컬에 클론하기

git 프로젝트에 참여하거나 원격 저장소(remote repository)를 로컬로 복사하려면 `clone`명령을 사용한다.

<pre>
/$ git clone https://github.com/realgrid/premium.git
</pre>



## staged상태가 된 파일들을 다시 untracted상태로 되돌리는 방법

아래 코드는 `git add .`으로 수정된 모든 파일을 staged상태로 만든 이후 특정폴더의 파일들(_drafts폴더)을 다시 untracted상태로 되돌리는 명령이다.
<pre>
/$ git reset HEAD _drafts/.
</pre>

<pre>
/$ git reset HEAD _posts/blog/2016-04-04-git-github-what-is-this.md
Unstaged changes after reset:
M   _posts/blog/2016-01-12-myfirst-slack-app.md
D   _posts/blog/2016-04-04-git-github-what's-this.md
</pre>

#### local에 만든 저장소를 서버 remote저장소와 동기화 한다.

우선 local 저장소에 remote 저장소를 추가한다.

<pre>
premium/$ git remote add origin https://onlydel@bitbucket.org/rgsuport/premium.realgrid.com.git
</pre>


#### remote저장소에 push했는데 commit user에 email주소가 없어 인증이 안된 상태??

<pre>
$ git config --global user.email "userid@userdomain.com"
</pre>

### 브랜치(branch)

**현재 브랜치 상태 보기**
<pre>
$ git branch {branch-name}
</pre>


**새로운 브랜치 만들기**
<pre>
$ git branch {branch-name}
</pre>

**브랜치 이동하기 = HEAD가 해당 브랜치를 가르키도록 하기**
<pre>
$ git checkout {branch-name}
</pre>

**브랜치 만들면서 이동하기**
<pre>
$ git checkout -b buggix
Switched to a new branch 'buggix'
</pre>

**브랜치 삭제하기**
<pre>
$ git branch -d buggix
Deleted branch buggix (was 3b295ae).
</pre>



**히스토리 로그 보기**
<pre>
$ git log --oneline --decorate --graph --all
* f15cc64 (HEAD -> dev-daelim) 대림 네번째 화면 구현
* 3b295ae (origin/master, origin/HEAD, master) 대림코퍼레이션 PS 폴더 추가 /  화면 3개 추가
* bb4cd5d js버전 템플릿 메인 페이지 수정
* 6225362 bmt: create skins folder for root
* 8643321 아이네피아bmt 수정
...
</pre>

---

**참조**

* [Slack API](https://api.slack.com){:target="_blank"}
