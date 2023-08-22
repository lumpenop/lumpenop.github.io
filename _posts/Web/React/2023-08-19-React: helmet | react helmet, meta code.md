---
date : YYYY-MM-DD HH:MM:SS +09:00
categories: [Web, React]
tags: [React]
published: true
---

## react-helmet-async

react-helmet 도 있지만
thread safe 이슈가 있어 react-helmet-async 를 사용한다고 한다

여러 스레드에서 동시 접근 시에도 안전한 결과를 보장하면 tread safe 하다고 한다

```
import { Helmet, HelmetProvider } from 'react-helmet-async';

const app = (
  <HelmetProvider>
    <App>
      <Helmet>
        <title>Hello World</title>
        <link rel="canonical" href="https://www.tacobell.com/" />
      </Helmet>
      <h1>Hello World</h1>
    </App>
  </HelmetProvider>
);
```

## meta tag
메타 태그는 웹페이지의 컨텐츠가 아닌 웹페이지의 정보를 명시하기 위한 메타 데이터를 담는 태그
head 태그 내에 배치된다

웹 페이지의 제목을 담는 title 태그와 meta 태그가 있다

### title 
title 은 주로 문서의 가장 큰 제목 태그와 일치시키는 경우가 일반적이고
브라우저 탭에도 노출되는 태그다
해당 페이지의 제목이 되며
20자 이내가 권장 사항

### meta
meta 태그는 타이틀을 제외한 모든 정보를 담게 된다

meta 태그의 name 속성으로 태그 종류를 구분하고
content 속성에 정보를 넣는다
content 에 들어갈 정보들은 콤마로 구분한다

#### description
```
<meta
  name="description"
  content="웹페이지에 대한 소개 글"
/>
```


#### keywords

```
<meta name="keywords" content="검색에 노출될 키워드1, 키워드2" />
```

#### author
```
<meta name="author" content="웹페이지 작성자" />
```


#### Open Graph 태그
og 태그라고 불리는 Open Graph 태그
Open Graph 프로토콜이라고 불리는 표준을 따라 웹페이지 컨텐츠 미리보기를 지원한다
Open Graph 는 링크 공유 등을 하였을 때 미리보기 카드를 제공할 때 사용된다


https://webclub.tistory.com/354
자세한건 이쪽에서 보자..
블로그 문 닫기 전에 정리해야지..