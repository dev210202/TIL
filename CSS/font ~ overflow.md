### Great Font pairings

1. 서로 보완된 글꼴 
2. 동일한 상위 패밀리 내에서 다른 글꼴 사용(lucda, lucida sans, lucida serif..)
3. 대비
4. 하나의 보스

### font property

### font 약식 속성
- font-style
- font-variant
- font-weight
- font-size(필수)/line-height
- font-family(필수)

### CSS icon
지정된 아이콘 클래스 이름을 인라인으로 element에 추가(i or span 태그)

### CSS link
링크는 모든 CSS 속성(color, font-family, background..)으로 스타일 지정 가능  
상태에 따라 스타일을 다르게 지정할 수 있음
- a:link - 방문하지 않은 정상적인 링크
- a:visited - 방문한 링크
- a:hover - 사용자가 위에 마우스를 놓았을 때의 링크
- a:active - 클릭하는 순간 링크

a:hover는 반드시 :link와 :visited 뒤에 와야함  
a:active는 반드시 :hover 다음에 와야함

#### text-decoration
링크에서 밑줄 여부를 설정하는 속성  
- none
- underline

### CSS 목록
정렬되지 않은 리스트(ul)
정렬된 리스트(ol)

#### list item marker
list-style-type으로 아이템의 마커를 설정 할 수 있음
- circle
- square
- upper-roman
- lower-alpha

#### image item marker
list-style-image로 아이템의 마커를 이미지로 설정할 수 있음

#### position item marker
list-style-position으로 마커 위치를 정할 수 있음

- outside(마커가 리스트의 바깥에 표시)
- inside(마커가 리스트의 안에 표시)

#### remove default settings
list-style-type:none을 사용해서 마커들을 제거 할 수 있음  
margin과 padding도 0으로 설정하여 없앨 수 있음

#### list 약식 속성
- list-style-type
- list-style-position
- list-style-image
속성중에 하나가 누락되면 누락된 속성의 기본값이 적용됨

### CSS Table

#### Table 테두리
border 속성을 사용


#### full-width table
tabel요소에 width:100%를 사용

#### collapse table borders
border-collapse: collapse를 사용해서 테두리를 단일로 만들 수 있음  
테이블 주위에 테두리만 지정하려면 table 태그에 border 속성만 지정하면 됨

### CSS Table Size

#### Table Width and Height
width와 height를 사용해서 너비와 높이를 설정

### CSS Table Alignment

#### Horizontal Alignment
text-align을 사용하여 수평으로 정렬할 수 있음
- left
- right
- center

#### Vertical Alignment
vertical-align을 사용하여 수직으로 정렬할 수 있음
- top
- bottom
- middle

### CSS Table Style

#### Table Padding
td, th 요소에 padding 속성을 사용

#### Horizontal Dividers
th, td 요소에 border-bottom 속성을 사용

#### Hoverable Table
tr:hover를 사용하여 마우스가 위로 올라왔을때 강조표시를 할 수 있음.

#### Striped Tables
nth-child()와 backgrond-color를 모든 짝수(혹은 홀수) 행에 사용한다.

#### Table Color
th요소에 background-color 사용

### CSS 반응형 테이블

#### CSS 반응형 테이블
화면이 모든 컨텐츠를 표시하기에 작을때 가로 스크롤 바가 표시된다.  
overflow-x:auto를 table주위 컨테이너 요소에 추가하여 반응형으로 만들 수 있음

### CSS Layout
display 속성은 요소가 어떻게 표시되는지를 특정시킴  
모든 요소는 유형에 따라 기본 표시값이 있음. 대부분 기본 표시값은 block or inline 

#### Block-level Elements
block-level 요소들은 항상 새줄에서 시작하고 모두 꽉찬 너비를 가진다.  
block-level 요소들의 예시는 다음과 같다  
- div
- h1 ~ h6
- p
- form
- header
- footer
- section

#### inline Elements
inline 요소는 새줄에서 시작하지 않고 필요한 만큼만 너비를 차지한다.
inline 요소의 예는 다음과 같다
- span
- a
- img

#### Display: none;
display: none;은 보통 javascript에서 요소를 삭제나 재창조 없이 숨기고 표시하기 위해서 사용된다.  

script 요소는 보통 display:none;으로 사용됨  

#### override the default display value
모든 요소에는 기본값이 있는데 이를 오버라이드 할 수 있다.

#### hide an element - display:none or visibility:hidden?
display 속성을 none으로 설정하여 요소를 숨길 수 있음  
visibility: hidden; 또한 요소를 숨기나 공간을 차지하고 레이아웃에 영향을 줌

### CSS Layout - width and max-width

#### Using width, max-width and margin: auto;
block-level의 요소가 언제나 전체 넓이를 가지는데 block-level에 설정하면 width 컨테이너의 가장자리까지 늘어나는 것을 막을 수 있음.

그 다음 여백을 자동으로 설정하여 컨테이너 내에서 요소를 수평으로 가운데 맞추게 된다.

요소는 지정된 너비를 차지하고 나머지 공간은 두 여백 사이에 균등하게 분할. 

위의 예시는 브라우저창이 요소의 너비보다 작을때 가로 스크롤이 생김.
이 상황에서 대신 max-width를 사용하면 브라우저가 작은창일때 처리방법이 향상됨.


### CSS Layout - position property
position 요소는 요소의 특정한 위치(static, relative, fixed, absolute or sticky)를 지정할때 사용함  

#### position property
position 속성은 5가지 위치값이 있음
- static
- relative
- fixed
- absolute
- sticky
그 다음 요소는 top, bottom, left, right 속성을 사용하여 배치됨.

#### position: static;
position의 기본값.  
top, bottom, left, right 속성의 영향을 받지않는다.

#### position: relative;
기본적인 위치에서 상대적으로 배치됨.  
top, bottom, left, right 속성에 의해 원래 위치에서 멀어지게 조정됨

#### position: fixed;
페이지가 스크롤 되더라도 항상 같은 위치에 유지됨.
일반적으로 위치한 페이지에 공백을 남기지 않음.

#### position: absolute;
가장 가까운 위치에 있는 부모를 기준으로 배치
하지만 부모에 지정된 상위 요소가 없다면 body의 요소를 사용하고 페이지 스크롤과 함께 이동함.

#### position: sticky;
사용자의 스크롤 위치를 기준으로 배치됨  
스크롤 위치에 따라 relative와 fixed 사이로 전환됨  
뷰가 주어진 오프셋위치에서 만날때까지는 상대적으로 배치되고 이후 그자리에서 고정됨  
또한 sticky가 작동하려면 top, right, bottom, left를 하나라도 지정해야 작동함.

### Positioning Text In an Image
그림에 텍스트 넣는 예시.

### CSS Layout - The z-index Property
z-index 속성은 요소의 스택 순서를 지정한다.

요소가 배치될때 다른 요소와 겹칠 수 있는데 z-index 속성으로 스택순서를 지정한다.  
z-index가 없으면 HTML 코드에서 마지막으로 정의된 요소가 맨 위에 표시된다.

### CSS Layout - Overflow
overflow 속성은 너무 커서 영역에 맞지 않는 콘텐츠를 제어함

#### CSS Overflow
overflow 속성에는 4가지가 있음
- visible (기본값, 오버플로가 잘리지 않고 요소 상자 외부에서 렌더링됨)
- hiden (오버플로가 잘리고 나머지 내용은 보이지않음.)
- scroll (오버플로가 잘리고 스크롤바가 추가되어 나머지 내용을 볼 수 있음)
- auto (scroll과 유사하짐나 필요할때만 스크롤바를 추가)

#### overflow-x, overflow-y
overflow-x와 overflow-y는 가로와 세로의 오버플로를 변경할지 여부를 정해준다.