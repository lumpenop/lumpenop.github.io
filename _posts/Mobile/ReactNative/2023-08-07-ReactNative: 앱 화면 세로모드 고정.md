---
date : YYYY-MM-DD HH:MM:SS +09:00
categories: [Mobile, ReactNative]
tags: [ReactNative]
published: true
---

## 가로, 세로모드
OS 별 설정 파일에서 앱의 가로, 세로 모드를 설정할 수 있다

- 가로모드 : landscape
- 세로모드 : portrait

### iOS
`ios/[프로젝트 이름]/Info.plist` 에서 아래 코드를 찾는다

```
<key>UISupportedInterfaceOrientations</key>
<array>
	<string>UIInterfaceOrientationPortrait</string>
	<string>UIInterfaceOrientationLandscapeLeft</string>
	<string>UIInterfaceOrientationLandscapeRight</string>
</array>
```

코드에서 필요한 부분만 남기고 주석처리를 하면 해당 모드만 사용이 된다



### Android

`android/app/src/main/AndroidManifest.xml`

```
<activity
  android:name=".MainActivity"
  android:label="@string/app_name"

  // 아래의 코드 추가
  android:screenOrientation="portrait"

  android:configChanges="keyboard|keyboardHidden|orientation|screenSize|uiMode"
  android:launchMode="singleTask"
  android:windowSoftInputMode="adjustResize">

```
