# Hoisting
함수 안에 있는 선언들을 모두 끌어올려서 해당 함수 유효 범위의 최상단에 끌어올리는 것

## 함수 Hoisting이 생겨난 이유
자바스크립트의 변수 생성과 초기화의 작업이 분리 돼서 진행 되기 때문이다.

```
console.log(a());
console.log(b());
console.log(c());

function a() {
    return 'a';
}

var b = function bb() {
    return 'bb';
}

var c = function() {
    return 'c';
}

---------------------
a
Uncaught TypeError: b is not a function
Uncaught TypeError: c is not a function

```
* 실제 자바 컴파일은 아래처럼 작동한다.
```
function a() {
    return 'a';
}
var b;
var c;
console.log(a());
console.log(b());
console.log(c());
 
b = function bb() {
    return 'bb';
}
c = function() {
    return 'c';
}
```

## 함수 표현식이 권장되는 이유
위의 a함수 예제처럼, 함수를 선언하기 전에 함수를 선언한 것이 되기 때문에, 코드의 구조가 엉성하게 만들기 때문이다. 함수 표현식을 권장한다.

[참고](https://deftkang.tistory.com/17)