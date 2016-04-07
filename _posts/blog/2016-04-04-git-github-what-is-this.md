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

**스테이지(stage)에 추가된 파일을 되돌리기**
<pre>
onlydel.github.com/$ git reset HEAD _posts/blog/2016-04-04-git-github-what-is-this.md
Unstaged changes after reset:
M   _posts/blog/2016-01-12-myfirst-slack-app.md
D   _posts/blog/2016-04-04-git-github-what's-this.md
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
