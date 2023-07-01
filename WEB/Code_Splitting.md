# Code Splitting

초기 로딩 시 번들 파일이 클 수록 느리게 페이지가 렌더링되는 걸 개선하기 위해서, 페이지마다 필요한 코드만 로딩하도록 코드를 잘게 나누는 것

### webpack 에서 설정하는 법

1. entry 설정을 이용한다
2. 기존 entry나 새로운 청크의 공통 의존성을 SplitChunksPlugin을 통해 제거하고 분할하는 방법
3. Dynamic import를 이용해 모듈에서 코드를 나누는 방법
