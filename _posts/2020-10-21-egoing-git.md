---
title: "생활코딩 Git수업"
excerpt: ""
date: 2020_10_21
categories: git
tags: git
last_modified_at: 2020-10-21 23:52:06
toc: true
toc_sticky: true
---

## 생활코딩 Git-CLI2(https://opentutorials.org/course/3839)  
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
- git commit -amend -m "msg"로 해당 커밋메시지 수정가능
- commit에 새 파일을 추가해서 수정하려면 아래와 같이 한다.
```git 
  git add <new filename>
  git commit --amend -m "new file also added"
  ```

### 5. git push
- commited 내용을 원격지에 보낸다.
- git push -f 로 원격지 내용을 강제로 덮어쓰기 가능

### 6. git diff
- commit이전에 변경된 내용을 보여준다.

### 7. git checkout
- 과거와 현재를 왔다갔다하며 시간여행
- 'git checkout master' 최신버전으로 돌아가기

### 8. git revert
- 특정커밋을 유지하면서 직전 커밋으로 돌아가려고 할때 사용한다.
일반적으로 reset 보다 안전한 커맨드로 자주 활용할듯
- revert는 역순으로 순차적으로 진행하지 않으면 충돌발생하여 수동으로 해결해야한다. 4번째 커밋에서 1번째로 revert하려면 4, 3, 2,순으로 순차적으로 revert하는게 충돌을 방지할 수 있다.

### 9. git reset
- Commit 취소할때
  - git reset --soft HEAD^ : 새로운 변경점을 staged한 상태로 되돌림
  - git reset --mixed HEAD^ : 새로운 변경점은 unstaged상태
  - git reset --hard HEAD^ : 새로운 변경점을 모두 삭제한 상태(직전 커밋 직후와 동일하게 되돌림)
