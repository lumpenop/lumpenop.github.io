---
date : YYYY-MM-DD HH:MM:SS +09:00
categories: [Mobile, ReactNative]
tags: [ReactNative]
published: true
---

iOS 에서 AsyncStorage 사용 시 몇 가지 에러가 발생

무슨 keyStore 로 해결하라는 이야기가 있는데
그건 근본적 원인을 해결해주지 못하고 아래와 같이 하는게 좋겠다

### NSCocoaErrorDomain Code=4

iOS 에서 AsyncStorage 가 이미 비어있는데 
`AsyncStorage.clear()` 를 시도할 경우 발생하는 에러

iOS 아래와 같이 `getAllKeys()` 와 `multiRemove()`를 함께 사용하여 `clear()` 대신 사용한다

```tsx
import {  Platform } from 'react-native';
import AsyncStorage from '@react-native-community/async-storage';

const asyncStorageKeys = await AsyncStorage.getAllKeys();
if (asyncStorageKeys.length > 0) {
  if (Platform.OS === 'android') {
    await AsyncStorage.clear();
  }
  if (Platform.OS === 'ios') {
    await AsyncStorage.multiRemove(asyncStorageKeys);
  }
}
```


### \[AsyncStorage] Passing null/undefined as value is not supported.

AsyncStorage 는 null 이나 undefined 값을 지원하지 않아 발생하는 에러

현재 서버와 통신하여 response 로 받은 값을 
사용하고 있어 아래와 같이 처리해줌

```tsx
if (response) {
  await Promise.all([
    AsyncStorage.setItem('data1', response.data1),
    AsyncStorage.setItem('data2', response.data2),
  ]);
}
```