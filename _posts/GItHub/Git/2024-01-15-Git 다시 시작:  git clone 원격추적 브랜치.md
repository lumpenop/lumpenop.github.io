---
date : YYYY-MM-DD HH:MM:SS +09:00
categories: [GitHub, Git]
tags: [Git]
published: true
---

## 원격 추적 브랜치
git 은 main 브랜치가 origin/main 과 연관되어 있다는걸 알고있다
이 연결은 두 가지 시나리오를 통해 뚜렷하게 확인할 수 있다

- pull 작업 도중 커밋들이 origin/main 에 받아지고 그 다음 main 으로 merge 된다
  merge 에서 내재된 타겟은 이 연결에서 결정된다

- push 작업 도중 main 브랜치의 작업은 origin/main (원격의 main 브랜치) 로 push 된다
  push 목적지는 main 과 origin/main 의 연결에서 결정된다

main 과 origin/main 사이 연결은 원격 추적 속성을 통해 설명할 수 있다
main 브랜치는 origin/main 브랜치를 추적하도록 설정되어 있다
-> main 이 merge 와 push 하기 위해 내재된 목적지가 생겼다는 뜻

이는 clone 시 자동으로 설정된다
clone 진행 시 원격 저장소에 있는 모든 브랜치에 대해 로컬에 원격 브랜치를 생성한다
그 후 저장소에서 현재 active 브랜치를 추적하는 로컬 브랜치를 생성한다 (대부분의 경우 main)

git clone 완료 시 하나의 로컬 브랜치를 가지게 된다
이후 원격 저장소의 여러 다른 브랜치도 확인할 수 있다 (로컬, 원격 양쪽에 활성화 된 상태가 된다)

```
local branch "main" set to track remote branch "o/main"
```
clone 시 위와 같은 명령을 볼 수 있는 이유와도 같다

스스로 임의 브랜치를 origin/main 혹은 다른 원격 브랜치를 추적하게 만들 수 있다
그러면 내재된 push merge 목적지를 갖게 되는 것이다

이 속성을 설정하는 방법은 두 가지인데


첫 번째는 지정한 원격 브랜치를 참조하는 새로운 브랜치를 생성, checkout 하는 방법이다
```
git checkout -b totallyNotMain origin/main
```

pull push 모두 적용 가능하다


두 번째는 git branch -u 옵션을 사용하는 방법이 있다

```
git branch -u origin/main foo
```
foo 브랜치가 origin/main 을 추적하도록 설정한다
foo 가 현재 작업중인 브랜치라면 생략 가능

