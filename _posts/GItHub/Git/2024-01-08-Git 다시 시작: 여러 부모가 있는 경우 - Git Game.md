---
date : YYYY-MM-DD HH:MM:SS +09:00
categories: [GitHub, Git]
tags: [Git]
published: true
---

## 여러 부모
merge 를 하면 부모가 여럿인 자식 커밋이 생긴다
이 때 부모를 선택하는 방법은 기존과 같다
다만 선택하는 순서에 횡 방향이 추가된다

```
git checkout main^2
```
실행 시 
현재 커밋의 바로 위 부모, 그 다음에 부모의 형제, 형제의 부모로 이동하게 된다

위 명령은 부모가 갈라지는 바로 밑 자식에서 해야 동작한다
갈라지는 포인트의 커밋까지 이동 후 해야 함


```
git checkout HEAD^2~2
```
위과 같이 연결해서 사용할 수도 있다
