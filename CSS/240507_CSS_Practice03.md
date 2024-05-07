<!-- 복습 -->
# 박스 모델

- CSS는 기본적으로 각각의 요소를 박스로 표현
- 부모의 박스 모델이 뭔지, 나의 박스 모델이 뭔지 꼭 체크해보기

### inline box

- a, span, em, strong 등과 같은 요소
- width, heigh 값에 영향받지 않음
- 컨텐츠 영역만큼만 차지
- 한 줄에 여러개의 인라인 박스를 배치할 수 있음

### block box

- h1, h2, p, div 등과 같은 요소는 기본적으로 블록
- width, heigh 값에 영향을 받아서 크기가 달라질 수 있다.

<br/>

### box-sizing

[지난 시간 TIL 참고](240503_CSS_Practice02.md)

<br/>

# 상속과 겹침 

### 상속 (inherit) 속성

- 크기나 규모에 영향을 주는 속성은 상속되지 않음
- 글자 크기, 색깔, 굵기, 글꼴 등 꾸미기 관련 속성은 상속이 됨
```css
/* h2를 green으로 만듦 */
h2 {
  color: green;
}

/* 부모 요소의 color를 사용하도록 sidebar 내의 h2를 홀로 남김 */
#sidebar h2 {
  color: inherit;
}
```
출처 : mdn web docs

<br/>

### 겹침 (cascade) 

- 순서대로 작성된 CSS 중 가장 마지막 규칙이 우선 반영
- `.` class 선택자 : 일반 스타일보다 더 우선순위가 높음
- `#` id 선택자 : 클래스 선택자보다 더 우선순위가 높음
- 인라인 스타일 : html에 `<style>` 태그로 직접 스타일을 선언한 것이 더 우선순위가 높음
- `!important` : 스타일 속성에 important가 선언되었다면 위치나 레벨에 관계없이 해당 스타일이 우선적으로 적용됨

<br/>

# 기본 선택자

### 전체 선택자

모든 요소를 선택

```css
/* Selects all elements */
* {
  color: green;
}
```

### 타입 선택자 (태그 선택자, 유형 선택자)

특정 태그를 선택

```css
/* All <a> elements. */
a {
  color: red;
}
```

### 클래스 선택자

태그 내 특정 클래스 네임을 가진 요소를 선택

```css
/* class="spacious" 인 요소 */
.spacious {
  margin: 2em;
}

/* <li> 태그 내에 class="spacious"인 요소 */
li.spacious {
  margin: 2em;
}

/* <li> 태그 내에 class 이름이 "spacious" 와 "elegant" 를 모두 포함한 요소 (and 조건) */
li.spacious.elegant {
  margin: 2em;
}
```

### ID 선택자

태그 내 특정 ID 값을 가진 요소를 선택

```css
/* id="demo" 요소 선택 */
#demo {
  border: red 2px solid;
}
```

### 그룹 선택자

여러 태그를 한번에 선택

```css
/* a와 span 태그를 모두 선택 */
a, span {
  background-color: DodgerBlue;
  color: #ffffff;
}
```

### 특성 선택자 (속성 선택자)

특정 태그가 있거나 특정 태그 안에 특정한 값이 있는 요소를 선택

```css
/* A href that contains "example.com" */
[href*='example.com'] {
  color: red;
}

/* A href that starts with https */
[href^='https'] {
  color: green;
}

/* A href that ends with .com */
[href$='.com'] {
  color: blue;
}
```