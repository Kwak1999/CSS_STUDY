# CSS속성

## 너비(width, height)

- 요소의 가로/세로 너비
- 기본값 -> auto 브라우저 너비를 계산
- 단위 -> px, em, vw 등 단위로 지정


- max-width, max-height
    - 요소가 커질 수 있는 최대 가로/ 세로 너비
    - none 최대 너비 제한 없음
    - auto 브라우저가 너비를 계산
    - 단위 px, em, vw 등 단위로 지정

## 단위

- px 픽셀
- % 상대적 백분율
- em 요소의 글꼴 크기
- rem 루트요소(html)의 글꼴 크기
- vw 뷰포트 가로너비의 백분율
- vh 뷰포트 세로 너비의 백분율

## 외부여백(margin)

- 요소의 외부 여백(공간)을 지정하는 단축 속성
- 음수를 사용할 수 있다
    - 외부 여백이 줄어든다


- 값을 하나 넣으면 모든 방향에 적용
- 두개를 넣으면 상하 좌우 적용
- 세개 넣으면 상 중 하 로 적용
- 네개 넣으면 시계방향으로 적용

## 내부여백(padding)

- 요소의 외부 여백을 지정하는 단축 속성
- 마진과 동일하게 값을 넣는 순서대로 적용
- 여백이 추가된 만큼 요소의 크기가 늘어남

## 테두리 선(border)

- 요소의 테두리 선을 지정하는 단축 속성


- 선-두께
    - 기본값 : medium


- 선-종류
    - 기본값: none
        - none
        - solid: 실선
        - dotted 점선
        - dashed 파선
        - double 두줄선
        - groove 홈이 파여있는 모양
        - ridge 솟은 모양
        - insert요소 전체가 들어간 모양
        - outset 요소 전체가 나온모양
      
      
- 선-색상
    - 기본값: black
        - 색상 표현(CSS전체 해당)
            - 색상이름
                - red, blue
            - Hex 색상코드
                - #000, #FFFFFF
            - RGB
                - rgb(255, 255, 0)
            - RGBA
                - rgba(0, 0, 0, 0.5
                    - 마지막 값은 투명도 0~1사이 값
                  

- 요소의 크기에 따라 같이 증가
- border-radius
    - 요소의 모서리를 둥글게 깎음
    - px 반지름

## box-sizing

- 요소의 내용(content)으로 크기 계산
- 요소의 내용 + padding + border로 크기 계산
- 요소의 크기 계산 기준을 지정

## overflow(넘침제어)

- 요소의 크기 이상으로 내용이 넘쳤을 때, 보여짐을 제어하는 단축 속성
- visible: 넘친 내용을 그대로 보여줌
- hidden: 넘친 내용을 잘라냄
- scroll: 넘친 내용을 잘라냄, 스크롤바 생성
- auto: 넘친 내용이 있는 경우에만 잘라내고 스크롤바 생성

## display

- 요소의 화면 출력(보여짐 )특성

- 각 요소에 이미 지정되어 있는 값
    - block: 상자(레이아웃) 요소
    - inline: 글자 요소
    - inline-block: 글자 + 상자 요소


- 따로 지정해서 사용하는 값
    - flex: 플렉스 박스(1차원 레이아웃)
    - grid: 그리드(2차원 레이아웃)
    - none: 보여짐 특성 없음, 화면에서 사라짐
    - 기타: table, table-row, table-cell 등

## opacity

- 요소 투명도
    - 1 불투명
    - 0~1 0부터 1사이의 투명

---
# 예제

  | 속성                         | 설명                | 예제                                            |
  | -------------------------- | ----------------- | --------------------------------------------- |
  | **width / height**         | 요소의 가로/세로 크기      | `div { width: 200px; height: 100px; }`        |
  | **max-width / max-height** | 요소의 최대 가로/세로 크기   | `img { max-width: 100%; max-height: 400px; }` |
  | **px 단위**                  | 픽셀 단위             | `div { width: 300px; }`                       |
  | **% 단위**                   | 부모 대비 백분율         | `div { width: 50%; }`                         |
  | **em 단위**                  | 요소 글꼴 크기 배수       | `p { font-size: 2em; }`                       |
  | **rem 단위**                 | 루트(html) 글꼴 크기 배수 | `p { font-size: 1.5rem; }`                    |
  | **vw 단위**                  | 뷰포트 가로너비 백분율      | `div { width: 50vw; }`                        |
  | **vh 단위**                  | 뷰포트 세로너비 백분율      | `div { height: 60vh; }`                       |
  | **margin (하나)**            | 모든 방향 외부여백        | `div { margin: 20px; }`                       |
  | **margin (두 개)**           | 상하/좌우 외부여백        | `div { margin: 10px 20px; }`                  |
  | **margin (세 개)**           | 상/좌우/하            | `div { margin: 10px 20px 30px; }`             |
  | **margin (네 개)**           | 상/우/하/좌           | `div { margin: 10px 20px 30px 40px; }`        |
  | **padding**                | 내부여백              | `div { padding: 10px; }`                      |
  | **border-width**           | 테두리 두께            | `div { border-width: 2px; }`                  |
  | **border-style**           | 테두리 종류            | `div { border-style: solid; }`                |
  | **border-color**           | 테두리 색상            | `div { border-color: red; }`                  |
  | **border (단축)**            | 테두리 한 줄 지정        | `div { border: 2px solid blue; }`             |
  | **border-radius**          | 모서리 둥글게           | `div { border-radius: 10px; }`                |
  | **box-sizing**             | 크기 계산 기준          | `div { box-sizing: border-box; }`             |
  | **overflow: visible**      | 넘친 내용 보임          | `div { overflow: visible; }`                  |
  | **overflow: hidden**       | 넘친 내용 숨김          | `div { overflow: hidden; }`                   |
  | **overflow: scroll**       | 넘친 내용 스크롤         | `div { overflow: scroll; }`                   |
  | **overflow: auto**         | 넘친 경우만 스크롤        | `div { overflow: auto; }`                     |
  | **display: block**         | 블록 요소             | `div { display: block; }`                     |
  | **display: inline**        | 인라인 요소            | `span { display: inline; }`                   |
  | **display: inline-block**  | 인라인+블록            | `img { display: inline-block; }`              |
  | **display: flex**          | 플렉스(1차원 레이아웃)     | `section { display: flex; }`                  |
  | **display: grid**          | 그리드(2차원 레이아웃)     | `div { display: grid; }`                      |
  | **display: none**          | 요소 숨김             | `div { display: none; }`                      |
  | **opacity 1**              | 불투명               | `div { opacity: 1; }`                         |
  | **opacity 0.5**            | 반투명               | `div { opacity: 0.5; }`                       |
  | **opacity 0**              | 완전투명              | `div { opacity: 0; }`                         |
