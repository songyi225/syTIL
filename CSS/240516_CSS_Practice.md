# Grid

display: grid 로 컨테이너에 그리드 지정

![flexandgrid](./css_images/flex%20&%20grid.png)

플렉스와 그리드의 차이
- flex 한 방향 레이아웃
- grid 두 방향 레이아웃

출처 : https://studiomeal.com/archives/533

---

### grid-template-rows, grid-template-column
- 컨테이너에 그리드 트랙의 크기를 지정해줌
- repeat 함수를 사용해서 몇 개의 행/열을 지정해줄지 결정할 수 있다!
```css
.container {
  display: grid;

  grid-template-columns: repeat(3, 1fr);
  /* repeat(반복횟수, 반복값) */

  grid-auto-rows: 100px;
  grid-gap: 20px;
}
```

---

### grid-template-areas
- 그리드 셀에 붙여진 이름을 가지고와서 직관적으로 배치하는 방법
```css
grid-template-areas:
    "header header"
    "sidebar content"
    "footer footer";
```

---

### grid-auto-rows, grid-auto-column

- 크기를 모를 때 자동으로 크기를 정해주는 속성
- 행/열 개수에 상관없이 지정한 크기대로 설정되고, minmax를 통해 최소 크기를 지정하고 자동으로 크기를 늘려줄 수 있다.
```css
grid-auto-rows: minmax(100px, auto);
```