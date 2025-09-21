## 기본 문법
---
- 선택자{속성 : 값;}
    - 선택자: 스타일을 적용할 대상
        - 기본 선택자
            - 전체 선택자 : *
            - 태그 선택자 : 태그 이름으로 요소를 선택
              - ex) li {}
            - 클래스 선택자 : class 속성의 값이 ~~ 인 요소 선택 '.' < 이 클래스
              - ex) .orange {} 이런 경우 `<li class="orange"></li>`의 선택자들이 적용 대상
            - 아이디 선택자: id 속성의 값이 ~~인 요소 선택
              - ex) #orange {} 이런 경우 `<li id="orange" class="orange"></li>`적용
        - 복합 선택자
            - 일치 선택자: 선택자 n개를 동시에 만족하는 요소 선택
              - ex) span.orange {}
            - 자식 선택자: ~~의 자식 요소를 선택
              - ex) ul > .orange {}
            - 하위 선택자: 선택자의 하위요소 선택
            띄어쓰기가 선택자의 기호
              - ex) div .orange {}
            - 인접 형제 선택자: 선택자의 다음 형제 요소 하나를 선택
              - ex) .orange + li {}
            - 일반 형제 선택자: 선택자의 다음 형제 요소 모두를 선택
              - ex) .orange ~ li {}
        - 가상 클래스 선택자
            - hover: 마우스 커서가 올라가 있는 동안 선택
              - ex) .box:hover {}
            - ACTIVE: 마우스를 클릭하고 있는 동안 선택
              - ex) .box:active {}
            - FOCUS: 포커스되면 선택
            ex) .input:focus {}
                - input
                - select
                - textarea
            - FIRST CHILD: 선택자가 형제 요소 중 첫째라면 선택
              - ex) .fruits span:first-child {}
            - LAST CHILD: 선택자가 형제 요소 중 막내라면 선택
              - ex) .fruits h3:last-child {}
            - NTH CHILD: 선택자가 형제 요소 중 n째라면 선택
              - ex) .fruits *:nth-child(2) {}
              - ex2) .fruits *:nth-child(2n) {} 단, n은 0부터 시작 0, 2, 4, 6 이런 식으로 진행
            - 부정 선택자: NOT 선택자 ~~가 아닌 요소 선택
              - ex) .fruits *:not(span) {}
        - 가상 요소 선택자
            - BEFORE: 선택자 요소의 내부 앞에 내용을 삽입.
              - ex) .box::before { content: "앞";}
            content 속성과 반드시 같이 사용
            - AFTER: 선택자 요소의 내부 뒤에 내용을 삽입
              - ex) .box::after { content: "뒤";} content 속성과 반드시 같이 사용
        - 속성 선택자
            - ATTR: 속성을 포함한 요소 선택
              - ex) [disabled] {}
            - ATTR=VALUE: 속성을 포함하고 값이 ~~인 요소 선택
              - ex) [type="password"] {}
    - 속성: 스타일의 종류
        - 스타일 상속
            - 부모에 스타일을 적용시킨다면 자식까지 같이 적용 되는 것
                - font-style: 글자 기울기
                - font-weight: 글자 두께
                - font-size: 글자 크기
                - line-height: 줄 높이
                - font-family: 폰트(서체)
                - color: 글자 색상
                - text-align: 정렬
                - ..등등
        - 강제 상속
            - 상속되지 않는 css 내용도 강제적으로 적용 시킴
                - 부모 요소를 내용을 상속받음
                ex) height: inherit;
    - 값: 스타일의 값
 
---

# CSS 선언 방식 & 선택자 우선순위 정리

## 1. CSS 선언 방식

| 방식 | 설명 | 예시 |
|-------|-------|-------|
| **내장 방식** | HTML 내부 `<style>` 태그에 CSS 작성 | `<style>div { color: red; margin: 20px; }</style>` |
| **인라인 방식** | HTML 요소에 `style` 속성을 직접 추가 | `<div style="color:red; margin:20px;"></div>` |
| **링크 방식** | HTML과 외부 CSS 파일 연결 | `<link rel="stylesheet" href="./css/main.css">` |
| **@import 방식** | CSS 문서 안에서 또 다른 CSS 문서를 불러오기 (link 방식 이후 적용) | `@import url("./box.css");` |

---

## 2. 선택자 우선순위 (Specificity)

점수가 높은 선언이 우선 적용됩니다.

| 선택자 | 점수 |
|---------|-------|
| 인라인 선언 | 1000점 |
| ID 선택자 | 100점 |
| Class 선택자 | 10점 |
| 태그 선택자 | 1점 |
| 가상 요소 선택자 | 1점 |
| 전체 선택자 | 0점 |
| 상속 | 점수 없음 |
| `!important` | 최상위 (9999999999점) |

- 점수가 같으면 **가장 마지막에 해석된 선언이 우선** 적용됩니다.

---

## 3. 핵심 정리

- **link 방식** → HTML과 CSS 연결 시 가장 일반적으로 사용  
- **@import 방식** → CSS 내부에서 또 다른 CSS 파일을 불러올 때 사용 (성능상 link 권장)  
- **우선순위 이해** → 충돌 시 어떤 스타일이 적용될지 쉽게 파악 가능  

