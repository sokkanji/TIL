# Skeleton

## Skeleton 이란?

2가지 의미가 있다. UI에서는 '로딩 중 보여주는 뼈대 화면'의 뜻으로 쓰이고
개발 문맥에서 프로젝트 템플릿, 기본 틀과 같은 최소 뼈대 구조를 뜻한다.

내가 오늘 처리한 건 Skeleton UI 의미인 **로딩 중 보여주는 뼈대 화면**이다.

## Skeleton 사용하게 된 이유

랜딩 페이지 로드될 때, 느린 네트워크에서 늦게 로드되는 이미지가 있어
이미지가 보여야 할 자리에 아무것도 뜨지 않아 사용자 경험이 좋지 못한 것을 개선하기 위해 Skeleton 처리를 해 보았다.

[유효 연결 타입](https://developer.mozilla.org/ko/docs/Glossary/Effective_connection_type)을 이용하여 느린 네트워크를 감지하는 훅도 만들었지만, 브라우저 지원성이 떨어져 최종적으로 사용할 수 없었다. 스크롤이 빠르고 한눈에 들어오는 모바일에서는 애니메이션을 끄는 걸로 논의가 되어 처리됐다. Skeleton이 적용하지 못했지만 기록용으로 남겨본다.

## 테스트 동영상

Skeleton을 적용할 거면 이미지를 감싸고 있는 엘리먼트까지 같이 처리하는 게 깔끔하다.

[skeleton 일반 네트워크 속도 버전 동영상 보기](../video/skeleton2.mov)

[skeleton 느린 네트워크 속도 버전 동영상 보기](../video/skeleton1.mov)

## 참고 문서

[Shadcn Skeleton](https://ui.shadcn.com/docs/components/skeleton)
