# Exercise 3

## Result

![alt result3](/exercise3/result3.png) <br/>

## Study Review

1. 각 Grid 항목에 개별 border를 적용하는 대신, Grid 컨테이너의 배경색과 gap 속성을 활용하여 border 효과 생성 가능

2. 한 줄로 나열된 여러 개의 Grid item중 중간 item의 가로 너비만 별도 설정 가능
   `grid-template-columns: repeat(4, 1fr) 1.5fr repeat(6, 1fr);`

3. 여러 개의 요소로 이루어진 block은 <ul> / <li> 태그 사용 권장
