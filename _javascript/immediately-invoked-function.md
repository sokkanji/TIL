# 즉시 실행 함수(Immediately-invoked_function_expression)
함수를 정의하자마자 바로 호출하는 함수

## 1. 즉시 실행 함수 사용법

### 기명 즉시 실행 함수

```
(function square(x) { 
    console.log(x*x); 
})(2); 

(function square(x) {
     console.log(x*x); 
}(2));
```
괄호의 위치가 조금 다를 뿐, 같은 기능을 수행한다.

### 익명 즉시 실행 함수 

```
(function (x) { 
    console.log(x*x); 
})(2); 

(function (x) {
     console.log(x*x); 
}(2));
```

### 변수에 즉시 실행 함수 저장

* 변수에 즉시 실행 함수 저장
```
(mySquare = function (x) { 
    console.log(x*x); 
})(2); 
mySquare(3);
```
<br/>

* 변수에 즉시 실행 함수 리턴값 저장
```
var mySquare = (function (x) { 
    return x*x; 
})(2); 
console.log(mySquare);
```
 mySquare는 즉시 실행 함수를 저장하고 있기 때문에 재호출이 가능하다.

## 즉시 실행 함수를 사용하는 이유

* 한 번의 실행만 필요로 하는 초기화 코드를 작성할 경우
* 첫 로드 시 초기화 할 때 변수를 전역으로 선언하고 싶지 않을 경우
* 라이브러리 전역 변수 충돌 방지

<br/>

[참고](https://beomy.tistory.com/9)