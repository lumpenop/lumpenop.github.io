---
categories: [GitHub, GitHub Pages]
tags: [GitHub, Pages]
published: true
---

### 깃허브 Pages 업데이트가 안될 때
깃허브 Pages 에서 jekyll 를 사용하면 local 에서 
_posts 폴더 내에 md 파일을 추가하여 글을 업데이트 할 수 있다

가끔 push 와 github actions deploy 까지 성공했는데도 
페이지에 반영되지 않는 경우가 있었다
그 때 마다 새로운 변경사항을 만들어서 다시 push 하곤 했었는데
어느 순간 먹통이 되었다

1. `_config.yml` 파일에 `futrue: true` 속성을 추가해준다
2. md 파일 설정에 `futrue: true` 추가

위 두가지 방법을 모두 사용하니 바로 update 되었음..



