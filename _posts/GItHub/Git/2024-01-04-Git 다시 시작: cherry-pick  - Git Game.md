---
date : YYYY-MM-DD HH:MM:SS +09:00
categories: [GitHub, Git]
tags: [Git]
published: true
---

## cherry-pick
HEAD 아래의 몇 커밋들에 대한 복사본을 만드는 것

```
git cherry-pick <Commit 1> <Commit 2>
```
rebase 와 비슷하지만
원하는 commit 을 선택할 수 있다

원하는 커밋이 무엇인지와 해시 값을 알 때 유용하다


## interactive rebase
원하는 커밋을 모르는 상황에서 사용한다
rebase 할 커밋들을 컴도할 수 있다

```
git rebase -i test
```

-i 옵션으로 인터랙티브 리베이스를 사용할 수 있다
인터랙티브 리베이스를 사용하면 목적지가 되는 곳 아래에 복사될 커밋들을 보여주는 텍스트 편집기를 띄운다
각 커밋을 구분할 수 있는 해시와 메시지도 보여준다

커밋의 순서를 바꾸거나
원하지 않는 커밋을 제외하고
여러 커밋을 합칠 수있다

```
git rebase -i HEAD~5
```
