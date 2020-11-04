# onload vs addEventListener

onload는 리소스들의 로딩이 완료되면 실행한다. 
### onload의 단점
1. 페이지 안의 이미지나 외부 파일이 로드 될때까지 기다린 후에 사용되어서 **로딩시간이 길어진다.**
2. 동일한 페이지 내에서 onload 함수는 **한 개만 존재해야한다.** (즉, 한 번만 실행된다는 뜻)
3. ```<body onload=""> ``` 와 같이 attribute가 설정 되어 있는 경우에는 **attribute만 작동하고, window.load는 작동하지 않는다.**
4. **다른 라이브러리 혹은 스크립트가 onload를 덮어씀**으로써 의도치 않은 오류를 일으키기 쉽다.

<br/>

### 이러한 onload의 단점을 대체하는 방법
``` 
window.addEventListener('onload', callback)
```

window.onload와 달리 addEvenListener를 사용한 경우 모든 콜백함수가 호출된다.

<br/>

### onload와 addEventListener 비교
```
window.onload = () => {
    console.log('A');
};
window.onload = () => {
    console.log('B');
};
----------------------------------------
B
```

```
window.addEventListener('load', () => {
    console.log('A');
});
window.addEventListener('load', () => {
    console.log('B');
});
----------------------------------------
A
B
```

<br/>

### 참고 사이트 <br/>
[mozilla_load](https://developer.mozilla.org/ko/docs/Web/Events/load) <br/>
[mozilla_addEventListener](https://developer.mozilla.org/ko/docs/Web/API/EventTarget/addEventListener)