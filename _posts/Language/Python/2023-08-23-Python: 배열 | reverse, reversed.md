---
date: YYYY-MM-DD HH:MM:SS +09:00
categories: [Language, Python]
tags: [Python]
published: true
---

### reverse

배열 함수로
원본 배열을 직접 수정하여 순서를 거꾸로 뒤집는다

```python
arr = [1, 2, 3]
arr.reverse()

print(arr) // [3, 2, 1]
```

### reversed

내장 함수로 원본 배열을 수정하지 않고 reversed or listreverseiterator 객체를 반환한다

```python
arr = [1, 2, 3]
reversedArr = list(reversed(arr))

print(reversedArr) // [3, 2, 1]
```

위 처럼 reversed 객체를 list 나 tuple 등으로 만들어줘야 자료형으로 사용 가능
