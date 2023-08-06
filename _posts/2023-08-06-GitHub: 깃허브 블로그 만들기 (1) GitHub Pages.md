---
categories: [GitHub, GitHub Pages]
tags: [GitHub, Pages]
---

# 깃허브 페이지 시작

깃허브 pages 는 깃허브에서 제공하는 호스팅 서비스라고 볼 수 있다
깃허브 저장소의 내용으로 웹 페이지를 구성해주는 서비스
블로그로도 많이 이용된다

### 1. 깃허브 저장소 생성 
`[username].github.io` 라는 이름으로 저장소를 생성한다
### 2. 로컬에서 저장소 클론
```
-
git clone https://github.com/[username]/[username].github.io
```

명령으로 깃허브 저장소를 내 컴퓨터에
### 3. index.html 작성

```
cd username.github.io
echo "Hello World" > index.html
```

### 4. 로컬 변경 사항 push
```
git add --all
git commit -m "Initial commit"
git push -u origin main
```

### 5. 웹에서 접속
`https://[username].github.io.` 
을 주소창에 입력하여 접속





