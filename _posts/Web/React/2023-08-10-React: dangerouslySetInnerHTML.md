---
date : YYYY-MM-DD HH:MM:SS +09:00
categories: [Web, React]
tags: [React]
published: true
---

## dangerouslySetInnerHTML

dangerouslySetInnerHTML 은 브라우저 DOM 에서
innerHTML 을 사용하기 위한 방법이다

코드에서 HTML 을 설정하는 것은 XSS 공격에 노출될 수 있어 위험하다
`__html` 속성에 데이터를 삽입한다

```tsx
-
<div dangerouslySetInnerHTML={{ __html: svg }} />
```

이렇게 사용하여 svg blob 파일을 div 에 주었다

