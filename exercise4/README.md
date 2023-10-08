## ✅ Exercise4 Result

![alt result4](/exercise4/result4.png)

## ✅ Study Review

- `text-shadow: offset-x offset-y blur-radius color` : 글자에 그림자 효과를 주는 속성

  - text-shadow를 여러 번 사용하여 글자 테두리 구현 가능 <br/>
    `text-shadow: -1px -1px 0 red, 1px -1px 0 red, -1px 1px 0 red, 1px 1px 0 red;` <br/>
    (1px은 외곽선이 자연스럽지만, 그 이상은 울퉁불퉁하게 구현된다.)

- align-items / align-content / align-self 비교
  - `align-items : center` : 1줄 일때, 수직축 기준으로 가운데 정렬
  - `align-content : center` : 2줄 이상 존재할 때, 수직축 기준으로 가운데 정렬
    예: 자식요소들이 두 줄로 존재할 경우,
    - align-items <br/>
      <img src="/exercise4/examples/align-items.png" width="250" height="150">
    - align-content <br/>
      <img src="/exercise4/examples/align-content.png" width="250" height="150">
  - `align-self : center` : 자식 요소들을 개별로 정렬 설정
    - 부모 컨테이너에 align-items가 설정되어 있을 때는 작동하지만,
    - align-content가 설정되어 있어 있을 때는 작동하지 않는다. <br/>
      <img src="/exercise4/examples/align-self.png" width="250" height="150"> <br/>

## ✅ References

- Web site design: landing page home page ui @Halo UI/UX for Halo Lab <br/>
  https://dribbble.com/shots/19627954-S-Studio-Website
