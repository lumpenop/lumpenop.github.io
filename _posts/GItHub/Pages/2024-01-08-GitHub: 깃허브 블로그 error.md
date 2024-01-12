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



### Branch "main" is not allowed to deploy to github-pages due to environment protection rules
위에서 default branch 를 main 으로 변경 후 
한 번 포스팅을 한 번 성공했지만
그 후로 위와 같은 에러 발생

Sounds like that your environment has some protection set up. You can try the following:

1. Go to you repository Settings.
2. Click on Environments.
3. Select your environment github-pages.
4. Next to Deployment branches select Selected branches from the dropdown.
5. Click on Add deployment branch rule.
6. Enter the pattern master.

This should allow deployments from the master branch to your github-pages environment.

git action 환경 설정을 수정해주지 않아 발생한 문제