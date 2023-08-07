---
date : YYYY-MM-DD HH:MM:SS +09:00
categories: [GitHub, GitHub Pages]
tags: [GitHub, Pages]
published: true
---



# 깃허브 Pages 업데이트가 안될 때
깃허브 Pages 에서 jekyll 를 사용하면 local 에서 
_posts 폴더 내에 md 파일을 추가하여 글을 업데이트 할 수 있다

가끔 push 와 github actions deploy 까지 성공했는데도 
페이지에 반영되지 않는 경우가 있었다
그 때 마다 새로운 변경사항을 만들어서 다시 push 하곤 했었는데
어느 순간 먹통이 되었다

## 해결

1. `_config.yml` 파일에 `futrue: true` 속성을 추가해준다
2. md 파일 설정에 `futrue: true` 추가

위 두가지 방법을 모두 사용하니 바로 update 되었다

### 그래도 안될 때가 있다..


#### 빈 커밋
```
git commit --allow-empty -m "rebuild"
git push origin master
```
위 명령으로 빈 커밋과 push 를 하여 Actions 를 새로 하거나


#### Actions 재실행
기존 Actions 의 jobs 를 다시 동작하게 하는 방법이 있다
깃허브 Actions 탭의 우측 상단에
![re-run.png](/assets/img/posts_images/re-run.png)

`Re-run all jobs` 버튼을 눌러 Actions 재실행

계속해서 빈 커밋을 생성하기 보다는 Actions 재실행으로
해결하는 편이 더 좋아보인다

`- layout home Index page -`
home 접속 시 빈 페이지가 보이는 이슈도 
Actions 재실행으로 해결할 수 있다


