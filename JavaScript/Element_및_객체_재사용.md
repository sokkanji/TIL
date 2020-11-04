# Element 및 객체 재사용 
### $(selector)
jQuery 객체

### document.getElemetById(id)
Document API 얻어낸 Element 객체

### 재사용하는 이유
jQuery 객체는 생성하는데 시간이 오래 걸리는 편이기 때문에, 재사용하는 편이 좋다.

ID로 접근해서 객체를 선택하는 경우에는 대부분 Element가 바뀌는 경우가 없으므로, 재사용하는 게 좋다.