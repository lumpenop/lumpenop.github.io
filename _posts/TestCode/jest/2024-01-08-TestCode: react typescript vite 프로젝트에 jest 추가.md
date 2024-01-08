---
date : YYYY-MM-DD HH:MM:SS +09:00
categories: [TestCode, jest]
tags: [jest]
published: true
---

### create vite typescript

`yarn create vite [프로젝트 명] --template react-ts`

`npm create vite@latest [프로젝트 명] --template react-ts`

## jest

### jest 설치
`yarn add -D jest @types/jest ts-node ts-jest @testing-library/react identity-obj-proxy jest-environment-jsdom @testing-library/jest-dom jest-svg-transformer`

### package.json

```json
"scripts":{
    ...
    "test": "jest"
 }
```

### jest.config.ts

root 폴더 하위
```ts
export default {
  testEnvironment: "jsdom",
  transform: {
    "^.+\\.tsx?$": "ts-jest",
  },
  moduleNameMapper: {
    "^.+\\.svg$": "jest-svg-transformer",
    "\\.(css|less|sass|scss)$": "identity-obj-proxy",
  },
  setupFilesAfterEnv: ["<rootDir>/jest.setup.ts"],
};
```

###  jest.setup.ts

root 폴더 하위

`import "@testing-library/jest-dom/extend-expect";`


```
module 에서 lint 에러가 발생 시 .eslintrc.cjs 파일에 아래 내용을 추가합니다.

module.exports = {
  env: {
    ...,
  	module: "node",
  }
}
```

### tsconfig.json
```
{
	"compilerOptions":{
      	...,
		"esModuleInterop": true      
    }
}
```
