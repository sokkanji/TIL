# img 비율 맞추기

### background-img 사용하는 경우

```
<!-- html -->
<div class="wrapper"></div>

<!-- css -->
.wrapper {
    width: 500px;
    height:500px;
    background-image: url();
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
}
```

### img 태그를 사용하는 경우

```
<!-- html -->
<div class="wrapper">
  <img src="./test.png" />
</div>

<!-- css-->
.wrapper {
  width: 500px;
  height: 500px;
}
img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
```
