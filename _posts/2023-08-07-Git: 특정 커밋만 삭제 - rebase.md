---
date : YYYY-MM-DD HH:MM:SS +09:00
categories: [GitHub, Git]
tags: [Git]
published: true
---

# 특정 커밋만 삭제하기
특정 커밋을 삭제해야 할 때 rebase 를 사용하면 편하다

```
-
git rebase -i [삭제할 커밋의 직전 커밋]
```

입력하면 가장 상단에 삭제할 커밋이 있고
pick 으로 최근 커밋들이 순서대로 정렬되어 있다

상단의 삭제할 커밋에 대해 pick 을 drop 으로 변경후
`:wq` 명령으로 문서를 저장한다

## conflict
리베이스 시 충돌이 일어날 경우 
충돌 해결 후 
```
-
git rebase --continue
```

> rebase 는 기존 커밋을 그대로 사용하는 것이 아니라
> 새로운 커밋으로 복사를 하는 것이기 때문에 remote 저장소에 이미 push 되어있는 커밋의 경우
> rebase 를 사용하지 않는 것이 좋다

그치만 나는 force push 로 밀어 넣어버림..

https://git-scm.com/book/ko/v2/Git-%EB%B8%8C%EB%9E%9C%EC%B9%98-Rebase-%ED%95%98%EA%B8%B0
