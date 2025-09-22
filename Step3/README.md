
# CSS속성2

## 글꼴
- font-style
    - 글자의 기울기
    - normal 기울기 없음
    - italic 이텔릭체 기울어진 글자
- font-weight
    - 글자의 두께
    - normal, 400 기본두께
    - bold, 700 두껍게
    - 100~ 900 백단위 숫자 9개
- font-size
    - 글자의 크기
    - 16px 기본크기
    - 단위 px, em, rem 등 단위로 지정
- line-height
    - 한 줄의 높이 행간과 유사
    - 숫자: 요소의 글꼴 크기의 배수로 지정
    - 단위: px, em, rem 등의 단위로 지정

## 문자
- color: 글자의 색상
    - rgb(0,0,0)
    - 색상: 기타 지정 가능한 색상
- text-align
    - 문자의 정렬방식
    - left 왼쪽 정렬
    - right 오른쪽 정렬
    - center 가운데 정렬
- text-decoration
    - 문자의 장식(선)
    - none 장식없음
    - underline 밑줄
    - line-through 중앙선
- text-indent
    - 문자 첫 줄의 들여쓰기
    - 0 들여쓰기 없음
    - 단위: px, em, rem 등 단위로 지정

## 배경
- background-color
    - 요소의 배경 색상
    - transparent 투명함
    - 색상: 지정 가능한 색상
- background-image
    - 요소의 배경 이미지 삽입
    - none 이미지 없음
    - url("경로") 이미지 경로
- background-repeat
    - repeat 이미지를 수직, 수평 반복
    - repeat-x 이미지를 수평 반복
    - repeat-y 이미지를 수직 반복
    - no-repeat 반복없음
- background-position
    - 요소의 배경 이미지 위치
    - 방향: top, bottom, left, right, center
    - 단위: px, em, rem
- background-size
    - 요소의 배경 이미지 크기
    - auto 이미지의 실제 크기
    - cover 비율을 유지, 요소의 더 넓은 너비에 맞춤
    - contain 비율을 유지, 요소의 더 짧은 너비에 맞춤
- background-attachement
    - 요소의 배경 이미지 스크롤 특성
    - scroll 이미지가 요소를 따라서 같이 스크롤
    - fixed 이미지가 뷰포트에 고정, 스크롤 x

## 배치
- position
    - 요소의 위치 지정 기준
    - static: 기준없음
    - relative: 요소 자신을 기준
    - absolute: 위치 상 부모 요소를 기준
    - fixed 뷰포트(브라우저)를 기준
    - 요소 쌓임 순서(Stack order)
        - 어떤 요소가 사용자와 더 가깝게 있는지(위에 쌓이는지) 결정
        - Sub title
            - 1. 요소에 position 속성의 값이 있는 경우 위에 쌓임(기본값 static 제외)
        - Sub title
            - 2. 1번 조건이 같은 경우, z-index 속성의 숫자 값이 높을 수록 위에 쌓임.
        - Sub title
            - 3. 1번과 2번 조건까지 같은 경우, HTML의 다음 구조일 수록 위에 쌓임.

## 플렉스(정렬)
- 1차원 레이아웃
- Flex Container의 화면 출력(보여짐) 특성
    - display
        - flex: 블록 요소와 같이 Flex Container 정의
        - inline-flex: 인라인 요소와 같이 Flex Container 정의
    - flex-direction
        - row: 행 축(수평)
        - row-reverse: 행 축 반전
        - column: 열 축(수직)
        - column-reverse: 열 축 반전
    - flex-wrap
        - nowrap: 묶음(줄 바꿈) 없음
        - wrap: 여러 줄로 묶음
    - justify-content
        - 주 축의 정렬 방법
            - flex-start: Flex Items를 시작점으로 정렬
            - flex-end: Flex Items를 끝점으로 정렬
            - center: Flex Items를 가운데 정렬
    - align-content
        - 교차 축의 여러 줄 정렬 방법
            - stretch: Flex Items를 시작점으로 정렬
            - flex-start: Flex Items를 시작점으로 정렬
            - flex-end: Flex Items를 끝점으로 정렬
            - center: Flex Items를 가운데 정렬
    - align-items
        - 교차 축의 한 줄 정렬 방법
            - stretch: Flex Items를 교차 축으로 늘림
            - flex-start: Flex Items를 각 줄의 시작점으로 정렬
            - flex-end: ""를 각 줄의 끝점으로 정렬
            - center: ""를 각 줄의 가운데 정렬
- items
    - order: Flex Item의 순서
        - 0: 순서 없음
        - 숫자: 숫자가 작을 수록 먼저
    - flex-grow
        - Flex Item의 증가 너비 비율
        - 0: 증가 비율없음
        - 숫자: 증가 비율
    - flex-shrink
        - Flex-Item의 감소 너비 비율
        - 1: Flex Container 너비에 따라 감소 비율 적용
        - 숫자: 감소비율
        - 0을 부여해준다면 공간이 부족해 디자인이 찌그러지는 현상을
          방지할 수 있다.
    - flex-basis
        - Flex Item의 공간 배분 전 기본 너비
        - auto: 요소의 Content 너비
        - 단위: px, em, rem 등 단위로 지정

## 전환
- transition
    - transition: 속성명 지속시간 타이밍함수 대기시간;
    - 요소의 전환(시작과 끝) 효과를 지정하는 단축 속성
    - transition-property
        - 전환 효과를 사용할 속성 이름을 지정
        - all: 모든 속성에 적용
        - 속성이름: 전환 효과를 사용할 속성 이름 명시
    - transition-duration
        - 전환 효과의 지속시간을 지정
        - 0s: 전환 효과 없음
        - 시간: 지속시간(s)을 지정
    - transition-timing-function
        - 전환 효과의 타이밍 함수를 지정
        - ease: 느리게 - 빠르게 - 느리게
          = cubic-bezier(0.25, 0.1, 0.25, 1)
        - linear: 일정하게 = cubic-bezier(0, 0, 1, 1)
        - ease-in: 느리게 - 빠르게 = cubic-bezier(0.42, 0, 1, 1)
        - ease-out: 빠르게 - 느리게 = cubic-bezier(0, 0, 0.58, 1)
        - ease-in-out: 느리게 - 빠르게 - 느리게 = cubic-bezier(0.42, 0, 0.58, 1)
    - transition-delay
        - 전환 효과가 몇 초 뒤에 시작할지 대기시간을 지정
        - 0s: 대기시간 없음
        - 시간: 대기시간(s)을 지정
- easing관련 사이트
    - https://easings.net/
      함수 차트
    - https://developer.mozilla.org/en-US/docs/Web/CSS/easing-function
      easing 함수 정보
    - https://gsap.com/docs/v3/Eases/
      트윈맥스

## 변환
- transform
    - 요소의 변환 효과
    - transform: 변환함수1 변환함수2 ...;
    - transform: 원근법 이동 크기 회전 기울임;
    - 2D 변환 함수
        - px
            - translate(x, y): 이동(x축, y축)
            - translateX(x): 이동 (x축)
            - translateY(y): 이동 (y축)
            - scale(x, y): 크기(x축, y축)
        - deg
            - rotate(degree) 회전 각도
            - skewX(x) 기울임(x축)
            - skewY(y) 기울임(y축)
    - 3D 변환 함수
        - px
            - perspective(n): 원근법(거리)
                - 원근법 함수는 제일 앞에 작성해야 정상 작동
                - 하위 요소를 관찰하는 원근 거리를 지정
                - 단위: px 등 단위로 지정
        - deg
            - rotateX(x): 회전(x축)
            - rotateY(y): 회전(y축)
        - backface-visibility
            - 3D 변환으로 회전된 요소의 뒷면 숨김 여부
            - visible: 뒷면 보임
            - hidden: 뒷면 숨김

---
# 예제


| 속성                             | 설명             | 예제                                                 |
| ------------------------------ | -------------- | -------------------------------------------------- |
| **font-style**                 | 글자의 기울기        | `p { font-style: italic; }`                        |
| **font-weight**                | 글자의 두께         | `p { font-weight: 700; }`                          |
| **font-size**                  | 글자의 크기         | `p { font-size: 20px; }`                           |
| **line-height**                | 한 줄의 높이(행간)    | `p { line-height: 1.5; }`                          |
| **color**                      | 글자 색상          | `p { color: rgb(255,0,0); }`                       |
| **text-align**                 | 글자 정렬          | `p { text-align: center; }`                        |
| **text-decoration**            | 글자 장식(선)       | `a { text-decoration: underline; }`                |
| **text-indent**                | 첫 줄 들여쓰기       | `p { text-indent: 2em; }`                          |
| **background-color**           | 배경 색상          | `div { background-color: lightblue; }`             |
| **background-image**           | 배경 이미지         | `div { background-image: url('bg.jpg'); }`         |
| **background-repeat**          | 이미지 반복 여부      | `div { background-repeat: no-repeat; }`            |
| **background-position**        | 배경 이미지 위치      | `div { background-position: center top; }`         |
| **background-size**            | 배경 이미지 크기      | `div { background-size: cover; }`                  |
| **background-attachment**      | 배경 스크롤 특성      | `div { background-attachment: fixed; }`            |
| **position: static**           | 기본 위치          | `div { position: static; }`                        |
| **position: relative**         | 자신 기준 위치       | `div { position: relative; top:10px; }`            |
| **position: absolute**         | 부모 기준 위치       | `div { position: absolute; left:50px; }`           |
| **position: fixed**            | 뷰포트 기준 고정      | `div { position: fixed; bottom:0; }`               |
| **z-index**                    | 쌓임 순서          | `div { z-index: 10; }`                             |
| **display: flex**              | Flex 컨테이너 정의   | `section { display: flex; }`                       |
| **flex-direction**             | Flex 아이템의 방향   | `section { flex-direction: column; }`              |
| **flex-wrap**                  | 줄 바꿈 여부        | `section { flex-wrap: wrap; }`                     |
| **justify-content**            | 주축 정렬          | `section { justify-content: center; }`             |
| **align-content**              | 교차축 여러 줄 정렬    | `section { align-content: flex-start; }`           |
| **align-items**                | 교차축 한 줄 정렬     | `section { align-items: center; }`                 |
| **order**                      | Flex 아이템 순서    | `.item { order: 2; }`                              |
| **flex-grow**                  | Flex 아이템 증가 비율 | `.item { flex-grow: 1; }`                          |
| **flex-shrink**                | Flex 아이템 감소 비율 | `.item { flex-shrink: 0; }`                        |
| **flex-basis**                 | Flex 아이템 기본 너비 | `.item { flex-basis: 200px; }`                     |
| **transition**                 | 전환(속성/시간 등 단축) | `div { transition: all 0.3s ease; }`               |
| **transition-property**        | 전환할 속성         | `div { transition-property: opacity; }`            |
| **transition-duration**        | 전환 지속시간        | `div { transition-duration: 2s; }`                 |
| **transition-timing-function** | 전환 타이밍         | `div { transition-timing-function: ease-in-out; }` |
| **transition-delay**           | 전환 대기시간        | `div { transition-delay: 1s; }`                    |
| **transform: translate**       | 이동             | `div { transform: translate(50px, 20px); }`        |
| **transform: scale**           | 크기 변경          | `div { transform: scale(1.5); }`                   |
| **transform: rotate**          | 회전             | `div { transform: rotate(45deg); }`                |
| **transform: skew**            | 기울임            | `div { transform: skewX(15deg); }`                 |
| **perspective**                | 3D 원근감         | `.container { perspective: 500px; }`               |
| **rotateX / rotateY**          | 3D 회전          | `.box { transform: rotateY(180deg); }`             |
| **backface-visibility**        | 뒷면 보임 여부       | `.box { backface-visibility: hidden; }`            |
