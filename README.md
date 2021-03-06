# CSS Flexbox



### 1. 특징

- 복잡한 계산 없이 간단함
- 매우 유연하며 반응형 구현 편리
- 정렬이 매우 간단
- 기존의 중앙정렬 번거로움이 해결
- IE, 구버전 브라우저에서는 적용이 힘듬



### 2. 배우는 이유

- 깔끔, 심플을 추구하는 요즘 트렌드에 적합
- 라이브러리, 프레임워크 없이 반응형 편리하게 구현
- 웹 어플리케이션에 어울리는 레이아웃
- 웹 말고도 많은 분야에서 사용하는 레이아웃 구조
- *React Native 에서 Flexbox 방식의 Style Sheet 사용



### 3. Reference 
- 최신의, 정확한 레퍼런스:
https://css-tricks.com/old-flexbox-and-new-flexbox/

- 많은 예제와 자세한 설명 MDN:
https://developer.mozilla.org/ko/docs/Web/CSS/CSS_Flexible_Box_Layout/Flexbox%EC%9D%98_%EA%B8%B0%EB%B3%B8_%EA%B0%9C%EB%85%90

- 마우스 클릭으로 많은 예제들을 직접 적용해보기
https://codepen.io/enxaneta/pen/adLPwv

- flexbox 익히기 게임: 
https://flexboxfroggy.com/#ko



---
### 사용법

#### 1. 구조
- ul, li 태그 처럼 감싸는 Wrapper 가 있고 그안에 Contents 가 들어있다.
- container > items 구조
- flex 레이아웃, 속성을 사용하려면 container display 속성에 flex 를 줘야한다.


#### 2. 속성
- Container :
  - display
    - flex 를 속성값으로 주면 flex 레이아웃 사용하겠다는 선언이다.
  - flex-direction 
    - default 로 row 정렬된다.
    - column 과 row 로 item 들의 레이아웃 설정 가능
    - column-reverse 와 row-reverse 는 item 들을 기본 속성과 반대로 정렬한다.
  - flex-wrap
    - wrap 을 속성값으로 주면 item 들의 넓이가 container 보다 클 때 밑으로 줄바꿈이 된다.
  - flex-flow
  - justify-content
    - 가로로 정렬하기 좋은 속성
    - flex-start: row 기준 item 들이 왼쪽으로 붙는다.
    - flex-end: row 기준 item 들이 오른쪽으로 붙는다.
    - center: row 기준 item 들이 가운데로 뭉친다.
    - space-between: row 기준 첫번째 item 은 왼쪽으로 붙고, 마지막 item 은 오른쪽으로 붙는 기준 모두 동일한 간격으로 정렬된다. (각자의 크기를 가지고 쫙 펼쳐진 느낌)
  - align-items
    - 세로로 정렬하기 좋은 속성
    - default 로는 stretch 속성값이 들어가며 direction: row 기준으로 item 들의 높이가 최대로 늘어나 꽉 채운다.
    - flex-start: row 기준 각자의 크기를 가지며 위로 붙는다.
    - flex-end: row 기준 각자의 크기를 가지며 밑으로 붙는다.
    - center: row 기준 각자의 크기를 가지며 세로로 가운데 정렬된다.
    - baseline: 컨텐츠들의 가상의 baseline 을 기준으로 맞춰준다.
  - align-content
    - item 그룹을 세로로 정렬하기 좋은 속성
    - justify-content 와 속성과 사용법이 거의 동일하며, 세로정렬 버전.

- Item :
  - order
  - flex-grow
    - 모든 item 에 일괄적으로 속성값을 1 로 설정하면 container 에 여백이 없게 약 1/x 씩 차지한다. 
    - 그 중 하나의 item 에만 2를 주면 그 item 만 약 2/x 을 차지한다.
  - flex-shrink
    - flex-grow 가 설정되지 않았으며, flex-basis 속성이 설정된 item 이 줄어들 때 줄어드는 비율을 설장한다.
    - 속성값으로 0 을 주면 item 의 col, row 넓이가 줄어들지 않으며 스크롤이 생긴다.
    - 속성값으로 1번 item 에 1 을 주고 2번 item 에 2를 주면 2번 item 이 약 2배 더 많이 줄어든다.
  - flex-basis
    - 300px 을 속성값으로 주면 절대값으로 그만큼의 col, row 넓이를 얻게 되는데 마치 max-width 를 설정 한 것 처럼 브라우저 크기에 따라 작아진다.
    - % 도 넣을 수 있다.
  - flex
    - 위에 속성을 축약으로 사용함 flex: flex-grow flex-shrink flex-basis;
  - align-self
    - container 속성인 align-items 를 개별 설정하고 싶을 때 쓰는 속성

##### ... 공부하면서 계속 업데이트


---
### 실습 예제

#### - Holy Grail Layout
   - 일반적인 Holy Grail Layout 를 flex 로 구현해보기

##### ... 공부하면서 계속 업데이트