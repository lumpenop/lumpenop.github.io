---
date: YYYY-MM-DD HH:MM:SS +09:00
categories: [Language, Javascript]
tags: [Javascript]
published: true
---

## Fetch API
axios 를 많이 사용하는 이유는 대부분 범용성 때문이라고 했다
axios 는 데이터를 자동으로 직렬화 해준다는 장점도 있다

하지만 fetch api 는 빌트인이기 때문에 추가로 설치할 것이 없고
성능에서 약간의 이점이 있다는 장점이 있다

### FormData
axios 에서 form data 전송 시

headers 내에 `'Content-type': 'multipart/form-data'` 설정과 
`transformRequest: data => data` 설정을 해주어야 했다


fetch 로 form data 전송 시에는 두 설정 모두 필요 없다


```tsx
body: formData,
```

바디 영역에 form data 를 넣어주기만 하면
브라우저에서 Content-Type 을 추론, 알아서 타입을 지정해준다고 한다

이 때 formData 의 형식은
`Content-Type: multipart/form-data; boundary=----WebKitFormBoundaryIn312MOjBWdkffIM`
이라는데 그냥 추론하는 편이 좋겠다

form data 는 직렬화를 진행하지 않는다는 점을 유의해야 한다

또한 서버와 form data name 만 잘 맞춰주면 내부에 파일 등을 넣어 전송할 수 있음









