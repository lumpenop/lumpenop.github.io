---
date : YYYY-MM-DD HH:MM:SS +09:00
categories: [GitHub, GitHub Pages]
tags: [GitHub, Pages]
published: true
---

### `The process '/opt/hostedtoolcache/Ruby/3.3.0/x64/bin/bundle' failed with exit code 5`

ruby version 문제

.github/workflows 폴더 내의 pages-deploy.yml 파일에서 
ruby-version 을 3.2 로 변경하여 해결

### index.html 뜨는 경우 혹은 게시글에만 404가 뜨는 경우
게시글에 404가 뜨는 경우는 현재 페이지가 index.html 만 뜨고 있는데
캐싱 되어 홈 화면이 보이는 것일 수 있다

index.html 뜨는 경우 
branch 명이 master 로 되어있지 않은지 확인해보고
master 라면 main 으로 브랜치 생성 후 
default branch 를 main 으로 변경 후 push



