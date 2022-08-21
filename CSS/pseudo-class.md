### Pseudo-classes
의사 클래스는 요소의 특수 상태를 정의하는데 사용
ex)
- 사용자가 요소위에 마우스를 놓을때
- 방문한 링크와 방문하지 않은 링크를 다르게 스타일지정
- 포커스를 받을때 요소 스타일 지정

#### Syntax
```
selector:pseudo-class {
  property: value;
}
```

#### Anchor Pseudo-classes
링크는 다양한 방식으로 표시될 수 있음
```
/* unvisited link */
a:link {
  color: #FF0000;
}

/* visited link */
a:visited {
  color: #00FF00;
}

/* mouse over link */
a:hover {
  color: #FF00FF;
}

/* selected link */
a:active {
  color: #0000FF;
}
```
a:hover가 효과적이려면 a:link와 a:visited 뒤에 와야함  
a:active는 효과를 나타내기 위해 a:hover 뒤에 와야함  
의사 클래스의 이름은 대소문자를 구분하지않음

#### Pseudo-classes and HTML Classes
의사 클래스는 HTML 클래스와 결합 할 수 있음
예시는 링크 위로 마우스를 가져가면 색상이 변경됨
```
a.highlight:hover {
  color: #ff0000;
}
```

#### Hover on <div>
div 요소에서 :hober 의사 클래스를 사용하는 예시
```
div:hover {
  background-color: blue;
}
```

#### Simple Tooltip Hover
div 요소위로 마우스를 가져가면 툴팁과 같은 p 요소가 표시되는 예시
```
p {
  display: none;
  background-color: yellow;
  padding: 20px;
}

div:hover p {
  display: block;
}
```

#### CSS - The :first-child Pseudo-class
:first-child 의사 클래스는 다른 요소의 첫번째 자식인 지정된 요소와 일치함

#### Match the first <i> element in all <p> elments
모든 p 요소의 첫번째 i요소와 매치시키게하는 예시
```
p i:first-child {
  color: blue;
}
```

#### Match all <i> elements in all first child <p> elements
첫번째 p 요소의 모든 i 요소와 매치시키게하는 예시
```
 p:first-child i {
  color: blue;
}
```

#### CSS - The :lang Pseudo-class
:lang 의사클래스를 사용하면 다른 언어에대한 특수 규칙을 정의할 수 있음  
예시는 lang="no"인 q 요소에 대해 따옴포를 정의함
```
<html>
<head>
<style>
q:lang(no) {
  quotes: "~" "~";
}
</style>
</head>
<body>

<p>Some text <q lang="no">A quote in a paragraph</q> Some text.</p>

</body>
</html>
```