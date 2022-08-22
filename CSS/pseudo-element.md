### CSS Pseudo-elements
의사 요소는 요소의 지정된 부분에 스타일을 지정되는데 사용됨  
ex)  
요소의 첫 글자 또는 줄 스타일 지정  
요소의 내용 앞이나 뒤에 내용 삽입

#### Syntax
```
selector::pseudo-element {
  property: value;
}
```

#### The ::first-line Pseudo-element
::first-line pseudo-element는 텍스트의 첫번째 줄에 특별한 스타일을 추가하는데 사용됨.  
::firest-line pseudo-element는 블록 수준 요소에만 적용할 수 있음 다음 속성은 ::first-line 의사요소에 적용됨
- font properties
- color properties
- background properties
- word-spacing
- letter-spacing
- text-decoration
- vertical-align
- text-transform
- line-height
- clear

::first-line과 :first-line 차이를 주의해야함  
이중 콜론은 CSS3에서 pseudo-elements의 단일 콜론 표기법을 대체했음  
이는 pseudo-classes와 pseudo-elements를 구분하기위한 W3C의 시도였음  

단일 콜론 구문은 CSS2 와 CSS1에서 pseudo-classes와 pseudo-elements 요소에 모두 사용됐었음.  

이전버전과의 호환성을 위해 단일 콜론 구문은 CSS2 및 CSS1 pseudo-elements에만 허용됨

#### The ::first-letter Pseudo-element
::first-letter pseudo-element는 텍스트의 첫글자에 특별한 스타일을 추가하는데 사용됨  
::first-letter 역시 블록 수준 요소에만 적용딤

#### Pseudo-elements and HTML Classes
pseudo-elements는 HTML 클래스와 결합할 수 있음

#### Multiple Pseudo-elements
여러개의 pseudo-element를 결합시킬 수 있음  

#### CSS - The ::before Pseudo-element
::before pseudo-element는 요소의 내용 앞에 일부 내용을 삽입하는데 사용됨

#### CSS - The ::after Pseudo-element
::after pseudo-element는 요소의 내용 뒤에 일부 내용을 삽입하는데 사용됨

#### CSS - The ::marker Pseudo-element
::marker pseudo-element는 목록 항목의 마커를 지정하는데 사용됨

#### CSS - The ::selection Pseudo-element
::selection pseudo-element는 사용자가 선택한 요소에 적용됩니다.  
::selection에 적용할 수 있는 CSS 속성은 color, background, cursor, outline입니다.