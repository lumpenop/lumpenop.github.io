---
date : YYYY-MM-DD HH:MM:SS +09:00
categories: [GitHub, Git]
tags: [Git]
published: true
---

## git tag
브랜치는 쉽게 변하고 임시적인 것이다
작업 히스토리에서 중요한 지점에 영구적으로 표시할 수 있는 방법으로
git tag 가 있다

git tag 는 커밋이 추가적으로 생성되어도 움직이지 않는다
특정 지점을 표시하고 있기 때문이다

커밋을 직접 지정하지 않으면 HEAD 지점에 tag 가 생성되고
지정했다면 해당 커밋에 tag 가 생성된다

```
git tag v1 [Commit]
```
v1 이라는 이름으로 태그를 생성하는데
태그로 체크아웃이 가능하지만 직접 커밋을 할 수 없다


## git describe
tag 가 닻 역할을 하고
tag 에서 얼마나 떨어져있는지를 알려주는 describe 명령이 있다

```
git describe [ref]
```
ref 에는 어떤 커밋이든 들어갈 수 있다
ref 를 특정하지 않으면 HEAD 를 기준으로 나타낸다


describe 의  출력은 아래와 같다
```
<tag>_<numCommits>_g<hash>
```
tag 는 가장 가까운 부모 태그
numCommits 은 얼마나 떨어져 있는지
hash 는 호출한 commit 의 hash 값을 말한다


