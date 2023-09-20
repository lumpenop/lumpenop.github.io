---
date : YYYY-MM-DD HH:MM:SS +09:00
categories: [Mobile, ReactNative]
tags: [ReactNative]
published: true
---

## api 성능 및 비용 개선을 위한 고민
모달 내에서 좋아요 <-> 좋아요 취소, 구독하기 <-> 구독 취소 등 
실시간으로 등록되어야 하는 것이 아니면서
여려번 눌러볼 수 있는 api 호출의 경우
모달을 띄워 연타를 하지 못하도록 했음에도 뭔가 찝찝한 부분이 있었다

화면 ui 는 실시간으로 반영되어야 하지만
api 의 경우는 모달이 닫힐 때 한 번만 실행되면 되는 것이 아닌가..?



### 고려해야 할 사항
1. 첫 진입 시 like 상태가 변경된 적 있는지
2. 좋아요 한 상태의 경우 unLike(), 좋아요 하지 않은 상태의 경우 like()

위 두 가지를 고려하여 코드를 작성했다

```typescript
useEffect(() => {
  return () => {
    if (isPressedButton) isLiked ? unLiked() : like()
  }
}, [modalVisible])
```

하지만 원하는데로 동작하지 않는다
useEffect 의 return 함수에서 (컴포넌트 unmount 시) 컴포넌트의 현재 상태를 추적하지 못한다 (첫 렌더 시 상태로 적용됨)

이럴 경우 useRef 를 사용하여 값을 기억해주면 좋다

```typescript
useEffect(() => {
  return () => {
    if (isPressedButtonRef.current) isLikedRef.current ? unLiked() : like()
  }
}, [modalVisible])
```