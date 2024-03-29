## 크로스 브라우징이란?

- 웹 페이지 개발할 때, 모든 브라우저에서 호환성 있게 올바르게 작동되게 하는 작업

- HTML, CSS, JavaScript 작성 시 W3C의 웹 규격에 맞는 코딩을 하여 어느 브라우저나 기기에서 사이트가 의도된 대로 작동되는 기법.

## 크로스 브라우징이 필요한 이유?

**브라우저마다 렌더링 엔진이 다르기 때문이다.**

- 작동되지 않는 HTML5, JavaScript 코드 존재
- 해석되지 않는 CSS 코드 존재
- 브라우저 버그들 존재
- 브라우저마다 자체적인 CSS 스타일

## IE를 버전마다 크로스 브라우징하는 이유?

최신버전으로 자동 업데이트가 되는 브라우저가 많으나 IE는 해당되지 않는다.
IE는 사용자가 직접 업데이트를 해야하며, 윈도우 버전에 따라 최대 버전이 한정되어있다.

## 렌더링 엔진(레이아웃 엔진)

- 페이지를 렌더링할 때 실질적으로 작업을 하게 되는 엔진
  같은 엔진을 사용하면 다른 브라우저에서도 비슷하게 출력된다.

- 레이아웃 엔진 종류
  |레이아웃 엔진 명| 사용하는 브라우저|만든 회사|
  |------|---|---|
  |트라이던트(Trident) | IE 등 사용| 마이크로소프트 |
  | 게코(Gecko) | 파이어폭스 사용| 모질라
  | 웹킷(Webkit) | 사파리, 크롬, iOS나 안드로이드 기본 브라우저들이 사용 | 애플|
  프레스토(Presto) | 오페라15버전부터 사용 X | 오페라 소프트웨어|
  블링크(Blink)| 크롬, 오페라 사용| 구글

## 브라우저 대응 순서

- 세계

1. Chrome
2. Safari
3. Firefox

[세계 점유율 조사 사이트](http://gs.statcounter.com/)

- 한국

1. Chrome
2. IE
3. Edge
4. Whale Brower
5. Safari
6. Firefox

[한국 점유율 조사 사이트](http://gs.statcounter.com/browser-market-share/desktop/south-korea/#monthly-201805-201903)

## 크로스 브라우징 작업

1. 사이트를 이용하여 브라우저에 맞게 작업한다. <br />
   https://caniuse.com/
2. CSS 초기화 작업 <br />
   브라우저마다 차이가 나는 기본 스타일 값들을 초기화 시킨다.

3. 메타 태그를 이용한 IE 모드

```
<head>
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
</head>
```
