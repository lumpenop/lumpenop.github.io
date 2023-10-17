---
date : YYYY-MM-DD HH:MM:SS +09:00
categories: [Mobile, ReactNative]
tags: [Android]
published: true
---

```
alias ioscleanall="rm -R /Users/[사용자 이름]/Library/Developer/Xcode/DerivedData;
rm -R ./livepickstar.xsworkspace;
rm ./Podfile.lock;
pod deintegrate;
pod cache clean --all;
pod install;
"

alias iosclean="pod deintegrate;
pod cache clean --all;
pod install
"

alias iosm1="pod deintegrate;
pod cache clean --all;
sudo arch -x86_64 gem install ffi;
pod install;
"
```