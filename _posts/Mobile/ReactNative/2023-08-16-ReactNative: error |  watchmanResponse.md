---
date : YYYY-MM-DD HH:MM:SS +09:00
categories: [Mobile, ReactNative]
tags: [ReactNative]
published: true
---

watchman 의 접근 권한이 부여된 상태이지만
권한이 없다는 에러

```
 watchmanResponse: {
    error: 'std::__1::system_error: open: /Users/...: Operation not permitted',
    version: '2022.09.26.00'
  }
```

내 경우에는 껐다 켜니까 잘 동작한다


#### 종료
```
watchman shutdown-server
```

#### 실행
```
watchman
```

위와 같이 해도 동작하지 않는다면
부여된 권한을 삭제 후 종료 - 실행
`설정 -> 개인정보 보호 및 보안 -> 파일 및 폴더 에서 watchman을 모두 삭제`
