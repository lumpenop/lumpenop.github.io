---
date: YYYY-MM-DD HH:MM:SS +09:00
categories: [Language, Typescript]
tags: [Typescript]
published: true
---

## 객체 타입의 타입 확장
원시 타입의 경우 타입 확장시 union 을 사용할 수 있지만
객체 타입의 경우 다르다

### interface
interface 로 작성된 객체 타입의 경우 타입 확장 시 
`extends` 로 상속을 이용한 확장과
재작성을 통한 확장이 가능하다
인터페이스는 같은 이름으로 재 작성 시 기존 정의된 목록에 
새로 작성된 인터페이스의 속성이 추가된다


### type
type 의 경우 `&` 연산자를 통해 확장이 가능하다




