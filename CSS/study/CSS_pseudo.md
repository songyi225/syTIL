# 가상 선택자 (pseudo-class selector)

`:` 또는 `::` 기호를 사용하여 선택한 요소에 스타일을 지정
- `: (의사 클래스)` : 특별한 상태일 때의 스타일링
- `:: (의사 요소)` : 선택한 요소의 일부분에 스타일링

### :cloud: 의사 클래스 (pseudo-class)

동적 의사 클래스(dynamic pseudo-classes)
- :link
- :visited
- :hover
- :active
- :focus

상태 의사 클래스(UI element states pseudo-classes)
- :checked
- :enabled
- :disabled

구조 의사 클래스(structural pseudo-classes)
- :first-child
- :nth-child
- :first-of-type
- :nth-of-type

기타 의사 클래스
- :not
- :lang

### 의사 요소 (pseudo-element)

하나의 선택자에 하나의 의사 요소만 지정할 수 있다.
```
selector::pseudo-element {
  property: value;
}
```
표준 의사 요소
- ::after
- ::backdrop
- ::before
- ::cue
- ::cue-region
- ::first-letter (:first-letter)
- ::first-line (:first-line)
- ::grammar-error 
- ::marker 
- ::part() 
- ::placeholder 
- ::selection
- ::slotted()
- ::spelling-error


## 참고 url

- http://www.ktword.co.kr/test/view/view.php?no=4273
- https://www.devkuma.com/docs/css/pseudo-element/
- https://velog.io/@chyori/CSS-%EC%9D%98%EC%82%AC-%ED%81%B4%EB%9E%98%EC%8A%A4
- https://developer.mozilla.org/ko/docs/Web/CSS/Pseudo-elements