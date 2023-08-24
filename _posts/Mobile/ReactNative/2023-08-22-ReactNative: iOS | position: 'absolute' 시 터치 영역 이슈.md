---
date : YYYY-MM-DD HH:MM:SS +09:00
categories: [Mobile, ReactNative]
tags: [iOS]
published: true
---

현재 modal 내부 코드 변경 시 바로 적용되지 않는 이슈가 있다..


position: 'absolute' 를 적용받는 영역 내부에 TouchableOpacity가 있다면
터치 영역이 밀려 올라가는 이슈가 있음
실 기기에서도 같은 이슈가 발생하면 다른 방안을 고려해봐야..