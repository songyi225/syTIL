# 반응형 웹

모바일, 데스크탑 뷰를 나누어서 유동적인 뷰를 만드는 연습 필요!

## flex box

- container : 내부 아이템들을 플렉스하게 배치할 수 있는 컨테이너
  - display
  - flex-direction
  - flex-warp
  - flex-flow
  - justfy-content
  - align-items
  - align-content
  
- items : 플렉스 컨테이너 안에 배치되는 아이템들
  - order
  - flex-grow
  - flex-shrink
  - flex-basis
  - flex
  - align-self
 
  
## flex 속성

하나의 플렉스 아이템이 자신의 컨테이너가 차지하는 공간에 맞추기 위해 크기를 키우거나 줄이는 방법을 설정하는 속성

- `flex-basis` : flex item의 기본 크기. 디폴트값으로는 해당 아이템의 width값을 가짐. width 값이 없으면 컨텐츠의 크기.
- `flex-grow` : flex-basis의 값보다 커질 수 있음. flex-basis를 제외한 여백 부분을 flex-grow에 지정된 숫자의 비율로 나누어 가진다.
- `flex-shrink` : 기본값은 1이기 때문에 언제나 flex-basis의 값보다 작아질 수 있다. 0으로 지정하면 작아지지 않기 때문에 고정폭으로 만들 수 있음.

위 속성을 따로 써도 되지만 축약형인 `flex` 를 써도 무방

```css
flex: 1;
/* flex-grow: 1; flex-shrink: 1; flex-basis: 0%; */

flex: 1 1 auto;
/* flex-grow: 1; flex-shrink: 1; flex-basis: auto; */

flex: 1 500px;
/* flex-grow: 1; flex-shrink: 1; flex-basis: 500px; */
```
