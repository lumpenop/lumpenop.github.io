---
date : YYYY-MM-DD HH:MM:SS +09:00
categories: [Mobile, ReactNative]
tags: [ReactNative]
published: true
---

# iOS 의 zIndex 적용 방식이 다르다

![Alt text](/Users/swk/Desktop/lumpenop.github.io/assets/img/posts_images/ReactNative/scroll_view_issue1.png)

위 사진에서 단일회차까지 상단 View 영역
복수회차부터 하단 View 영역에 닿게 된다

drop down 영역에 `position: absolute`, `zIndex` 도 주었지만 
하단 View 영역에 우선 순위가 있다

iOS 에서의 zIndex 는 같은 레벨에서만 적용되기 때문이었다


https://velog.io/@nakta/React%EC%97%90%EC%84%9C-z-index-%EA%B4%80%EB%A6%AC%ED%95%98%EA%B8%B0
이런 것도 함께 고려해보면 좋을듯 하다

