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


---

**참조**

* [Slack API](https://api.slack.com){:target="_blank"}
