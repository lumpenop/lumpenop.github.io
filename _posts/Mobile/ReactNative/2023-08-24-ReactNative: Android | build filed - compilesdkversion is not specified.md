---
date : YYYY-MM-DD HH:MM:SS +09:00
categories: [Mobile, ReactNative]
tags: [Android]
published: true
---

# compilesdkversion is not specified

원래는 compilesdkversion 이 맞지 않아 project 수준 build.gradle 에서 
compilesdkversion 설정을 해주어야 하는 에러이지만

나의 경우에는
npm dependencies 이슈였다..

`mode_modules` 를 제거하고 `npm install` 을 다시 실행하여 해결

# 500 error
`npm install` 후에

500 error 가 떴느데
npm 의존성 버전 업이 되면서 새 버전이 설치된 이슈였다
몇 가지 패키지가 자동 설치되지 않으면서
새로 설치할 때 버전을 지정하지 않아서 생긴 이슈..

개별 설치 시에 버전을 잘 확인해야 함
