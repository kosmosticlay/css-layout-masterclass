## ✅ Exercise Result

![alt result1](/exercise1/result1.png)

## ✅ Study Review

- (Grid item안에 아무리 내용의 양이 적어도) 최소한 100px, 최대 자동(auto)으로 세로 길이가 늘어나도록 처리 <br/>
  `grid-template-rows : repeat(3, minmax(100px, auto))`

- auto-fill / auto-fit 차이
  - `auto-fill` : 셀의 수가 초기 설정보다 모자라면, 빈 자리는 공간이 빈 상태 그대로 존재 <br/>
    `grid-template-columns: repeat(auto-fill, minmax(20%, auto))`
  - `auto-fit` : 셀의 수가 초기 설정보다 모자라면, 빈 자리는 나머지 셀이 차지 <br/>
    `grid-template-columns: repeat(auto-fill, minmax(20%, auto))`

## ✅ References

- Education Courses App @Andrew Sereda <br/>
  https://dribbble.com/shots/19526780-Education-Courses-App
