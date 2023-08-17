---
date : YYYY-MM-DD HH:MM:SS +09:00
categories: [IDE, VSCODE]
tags: [VSCODE]
published: true
---


# 저장 시 eslint, prettier 설정

#### Format On Save
`command + ,` 를 눌러서 설정 진입 후 `Format On Save` 설정을 켜준다

#### settings.json
settings.json 파일 내에
```
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  }
```
설정 추가

