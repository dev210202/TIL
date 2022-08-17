### CSS 윤곽선
윤곽선은 element를 더 눈에띄게 만들기 위해 border 주위에 그려지는 선.

속성
- outline-style
- outline-color
- outline-width
- outline-offset
- outline

#### outline-style
- dotted
- dashed
- solid
- double
- groove
- ridge
- inset
- outset
- none
- hidden

#### outline-width
- thin (일반적으로 1px)
- medium (일반적으로 3px)
- thick (일반적으로 5px)
- 특정 사이즈(px, pt, cm, em, etc)

#### outline-color
- name
- hex
- rgb
- hsl
- invert (색상 배경에 관계없이 윤곽선 표시)

#### outline 약식
- outline-width
- outline-style(필수)
- outline-color

#### outline-offset
outline-offset은 outline과 border사이에 공간을 추가하는 속성이다.  
outline과 border사이의 공간은 투명하다.

### CSS text

#### color
- name
- hex
- rgb

#### text alignment
text-align 속성은 element를 수평 정렬하는데 사용된다.
- left
- center
- right
- justify (모든 줄의 너비가 동일하고 요소의 너비와 동일하게 직선 정렬)

#### text-align-last
text-align-last 속성은 텍스트의 마지막 줄을 정렬하는 방법을 지정한다.  
들어갈 수 있는 값은 text-align과 동일

#### text direction
direction과 unicode-bidi 속성을 사용하여 element의 텍스트 방향을 변경 할 수 있음.  

direction
- ltr (left to right)
- rtl (right to left)

unicode-bidi
- bidi-override (글자를 오른쪽에서 왼쪽으로 출력, dircetion:rtl과 써야 효과가 나옴)

### vertical-align
vertical-align은 element의 수직 정렬을 설정하는데 쓰인다.
- baseline (부모의 기준선에 맞춰정렬)
- text-top (상위 요소에 맞춰 정렬)
- text-bottom (하위 요소에 맞춰 정렬)
- sub (부모의 아래 첨자 기준선에 정렬)
- super (부모의 위 첨자 기준선에 정렬)
- top (줄에서 가장 높은 요소의 맨위에 정렬)
- middle (부모 요소의 중간에 배치)
- bottom (줄에서 가장 낮은 요소에 정렬)
- length (px, cm, etc)
- %

### CSS Text decoration

#### text-decoration-line
text-decoration-line은 텍스트에 데코를 추가하는데 사용됨
- overline (텍스트 위에 줄 표시)
- line-through (텍스트 중간에 통과하게 줄 표시)
- underline (텍스트 밑에 줄 표시, 링크가 아닌 줄에 밑줄을 긋는건 권장되지 않음)
- overline underline (텍스트 위 아래에 줄 표시)

#### text-decoration-color
text-decoration-color는 장식선의 색상을 설정하는데 사용됨

#### text-decoration-style
text-decoration-style은 장식선의 스타일을 지정하는데 사용됨

#### text-decotaion-thickness
text-decotaion-thickness은 장식선의 선 굵기를 지정하는데 사용됨

#### text-decoration 약식 속성
- text-decoration-line (필수)
- text-decoration-color
- text-decoration-style
- text-decoration-thickness

#### 링크 지우기
HTML의 모든 링크는 기본적으로 밑줄이 그어짐. 링크에 밑줄을 없애려면 text-decoration: none;을 사용

### CSS Text Transform

#### text-transform
텍스트에서 대문자와 소문자를 지정하는데 사용됨
- uppercase (모두 대문자)
- lowercase (모두 소문자)
- capitalize (각 단어의 첫 글자를 대문자로 바꿈)

### CSS Text Spacing

#### text-indent
첫번째 줄 들여쓰기를 지정하는데 사용

#### letter-spacing
문자 사이의 공백을 지정하는데 사용

#### line-height
줄 사이의 공백을 지정하는데 사용

#### word-spacing
단어 사이의 공백을 지정하는데 사용

#### white-space
element 내부의 공백을 처리하는데 사용

### CSS Text Shadow

#### text-shadow
텍스트에 그림자를 추가할때 사용  
text-shadow: [horizontal shadow] [vertical shadow] [blur] [color]


### CSS Fonts
일반적인 글꼴들
- serif
- sans-serif
- monospace
- cursive
- fantasy

#### font-family
텍스트의 폰트를 지정하는데 사용  
글꼴 이름이 2단어 이상이면 따옴표로 묶어줘야함.
글꼴 지정시 대체 시스템으로 여러가지 글꼴을 포함해야함.  

### CSS Web Safe Fonts
web safe fonts는 모든 브라우저와 장치에 보편적을 설치되는 글꼴임.  

그러나 100% 완전히 안전한 글꼴은 없음. 따라서 대체 글꼴을 사용하는게 굉장히 중요.  

HTML과 CSS에서 베스트 안전 글꼴은 다음과 같음
- Arial (sans-serif)
- Verdana (sans-serif)
- Helvetica (sans-serif)
- Tahoma (sans-serif)
- Trebuchet MS (sans-serif)
- Times New Roman (serif)
- Georgia (serif)
- Garamond (serif)
- Courier New (monospace)
- Brush Script MT (cursive)


### CSS Font Fallbacks

#### 일반적으로 사용되는 폰트 대체들
- Serif
- Sans-serif
- Monospace
- Cursive
- Fantasy

### CSS Font Style

#### font-style
주로 기울임꼴 텍스트를 지정하는데 사용
- normal
- italic (기울임)
- oblique (italic과 유사하나 덜 지원해줌)

#### font-weight
글꼴의 두께를 지정하는데 사용
- noraml
- lighter
- bold

#### font-variant
텍스트를 작은 대문자로 표시할지 여부를 지정하는데 사용  
small-cpas는 모든 소문자를 대문자로 변환하는데 변환된 대문자는 텍스트의 원래 대문자보다 작은 글꼴 크기로 나타남.

### CSS font size

#### font-size
텍스트의 크기를 설정하는데 사용  
절대크기, 상대크기일 수 있다.

절대크기(absolute)
- 텍스트를 지정한 크기로 설정함
- 사용자가 모든 브라우저에서 텍스트 크기를 변경하는 것을 허용하지 않음(접근성의 이유로 좋지않음)

상대적크기(relative)
- 주변 element를 기준으로 크기 설정
- 사용자가 브라우저에서 텍스트 크기 변경가능

#### pixel
픽셀로 설정하면 사용자가 텍스트 크기를 제어할 수 있음

#### em
사용자가 브라우저 메뉴에서 텍스트 크기를 조정할 수 있도록 하기위해 많은 개발자가 px 대신 em을 사용함  
1em은 현재 글꼴 크기인데 기본적으로 16px임

#### 반응형 글꼴 크기
단위로 vw을 설정하면 텍스트 크기가 브라우저 창의 크기를 따름  
1vw는 브라우저창의 크기의 1%

### CSS google fonts
<head> 섹션에 스타일 시트를 추가하고 css에서 글꼴을 참조하면 된다.
```
<head>
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Sofia">
<style>
body {
  font-family: "Sofia", sans-serif;
}
</style>
</head>
```

여러개를 사용하려면 |를 사용해서 구분한다.


#### 글꼴 효과 활성화
effect=[effectname]을 사용해서 글꼴 효과를 활성화할 수 있음  
효과도 마찬가지로 |를 사용해서 여러개를 쓸 수 있다.
