# slick slider 라이브러리

### slick

slick slider는 반응형 웹을 지원하는 슬라이더 라이브러리

### slick 다운로드 및 파일 로드

```
<link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/npm/slick-carousel@1.8.1/slick/slick.css"/>
<script type="text/javascript" src="https://cdn.jsdelivr.net/npm/slick-carousel@1.8.1/slick/slick.min.js"></script>
<!-- import jQuery CDN -->
```

### HTML

```
<div>
  <div id="slider">
    <div>1</div>
    <div>2</div>
    <div>3</div>
    <div>4</div>
    <div>5</div>
    <div>6</div>
    <div>7</div>
    <div>8</div>
    <div>9</div>
    <div>10</div>
  </div>
</div>
```

### JS

```
<script>
  $(function(){
    $('#slider').slick({
      slide: 'div',		//슬라이드 되어야 할 태그 ex) div, li
      infinite : true, 	//무한 반복 옵션
      slidesToShow : 4,		// 한 화면에 보여질 컨텐츠 개수
      slidesToScroll : 1,		//스크롤 한번에 움직일 컨텐츠 개수
      speed : 100,	 // 다음 버튼 누르고 다음 화면 뜨는데까지 걸리는 시간(ms)
      arrows : true, 		// 옆으로 이동하는 화살표 표시 여부
      dots : true, 		// 스크롤바 아래 점으로 페이지네이션 여부
      autoplay : true,			// 자동 스크롤 사용 여부
      autoplaySpeed : 10000, 		// 자동 스크롤 시 다음으로 넘어가는데 걸리는 시간 (ms)
      pauseOnHover : true,		// 슬라이드 이동	시 마우스 호버하면 슬라이더 멈추게 설정
      vertical : false,		// 세로 방향 슬라이드 옵션
      prevArrow : "<button type='button' class='slick-prev'>Previous</button>",		// 이전 화살표 모양 설정
      nextArrow : "<button type='button' class='slick-next'>Next</button>",		// 다음 화살표 모양 설정
      dotsClass : "slick-dots", 	//아래 나오는 페이지네이션(점) css class 지정
      draggable : true, 	//드래그 가능 여부

      responsive: [ // 반응형 웹 구현 옵션
        {
          breakpoint: 960, //화면 사이즈 960px
          settings: {
            //위에 옵션이 디폴트 , 여기에 추가하면 그걸로 변경
            slidesToShow:3
          }
        },
        {
          breakpoint: 768, //화면 사이즈 768px
          settings: {
            //위에 옵션이 디폴트 , 여기에 추가하면 그걸로 변경
            slidesToShow:2
          }
        }
      ]

    });
  })
	</script>
```

### slider 함수

- slider 제거

```
$('#slider-div').slick("unslick")
```

이미 만들어진 slick을 제거한 후 다시 slick 해야 제대로 작동함.

- slider에 새로운 아이템 추가

```
$('#slider-div').slick('slickAdd',"<div>새로운 아이템</div>");
```

- 자동 슬라이드 넘기기 정지 및 시작

```
$('#slider-div').slick('slickPause');    // 정지
$('#slider-div').slick('slickPlay');    // 시작

```

[참고 블로그](https://programmer93.tistory.com/34)
