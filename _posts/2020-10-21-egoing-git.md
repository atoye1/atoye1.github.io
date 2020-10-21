---
title: "생활코딩 Git수업"
excerpt: ""
date: 2020_10_21
categories:
tags:
last_modified_at: 2020-10-21 23:52:06
toc: true
toc_sticky: true
---

## 기본 명령어

### 1. git init

- 깃 저장소를 시작

### 2. git log

- 커밋 기록들을 본다
- git log --stat
  - 해당 커밋에서 수정된 파일 목록과 수정사항통계를 보여준다.
- git log -p
  - 수정된 내용까지 모두 보여준다

### 3. git add
- unstaged 된 파일을 staged한다.
- git reset 으로 취소가능
- git reset --hard 전체 내용을 변경전(직전 커밋으로) 되돌린다.

### 4. git commit
- staged된 내용을 커밋한다.
- git commit -am "msg" 와 같이 사용간능

### 5. git push
- commited 내용을 원격지에 보낸다.

### 6. git diff
- commit이전에 변경된 내용을 보여준다.

### 7. git checkout
- 과거와 현재를 왔다갔다하며 시간여행
- 'git checkout master' 최신버전으로 돌아가기
