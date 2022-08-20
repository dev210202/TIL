### CSS Layout - display: inline-block
display: inline과 display: inline-block의 차이점
1. 요소의 너비와 높이를 설정 할 수 있음 
2. 위쪽 및 아래쪽 마진과 패딩이 고려됨
3. 요소 뒤에 줄바꿈을 추가하지 않으므로 다른 요소 옆에 배치할 수 있음

#### using inline-block to create navigation links
display: inline-block으로 네비게이션을 세로 대신 가로로 표시할 수 있음

### CSS Layout - Horizontal & Vertical Align
marginL auto - block 요소(div)를 수평으로 가운데에 맞춤  
너비를 설정하면 지정된 너비를 차지하고 나머지 공간이 두 여백 사이에 균등하게 분배됨

#### Center Align Text
text-align: center - 요소 내부의 텍스트를 가운데로 정렬함

#### Center an Image
이미지를 가운데에 맞추려면 왼쪽과 오른쪽 마진을 auto로 설정하고 block요소로 만듬

#### Left and Right Align - Using position
postion: absolute를 사용해서 위치를 정렬함  
다른 방법으로는 float 속성을 사용 할 수 있음

#### The clearfix Hack
요소가 부모 요소보다 크고 float된 경우 컨테이너 외부로 overflow됨 이를 clearfix hack을 사용해서 해결할 수 있음

#### Center Vertically - Using padding
요소를 세로로 가운데에 맞추는 방법중 가장 간단한 방법은 상단과 하단의 패딩을 사용하는것.  
수평 수직으로 가운데에 맞추려면 padding과 text-align:center를 사용함 
다른 트릭으로는 line-height를 사용하여 height값과 동일한 값으로 맞추는 방법이 있음

#### Center Vertically - Using position & transform
padding과 line-height를 사용하지 않는경우 다른 방법으로는 position과 transform 속성을 사용하는 방법이 있음

#### Center Vertically - Using Flexbox
flexbox를 사용하는 방법도 있음. 대신 IE10및 이전버전에서 지원되지 않음.

### CSS Combinators
combinator는 선택자들의 관계를 설명하기위한 것임  
CSS selector는 둘 이상의 단순 선택자를 포함할 수 있음 단순 선택자 사이에 combinator를 포함할 수 있음.  
combinator는 4가지가 있음
- 자손 선택자 (space)
- 자식 선택자 (>)
- 인접한 형제 선택자 (+)
- 일반 형제 선택자 (~)


#### Descendant Selector
자손 선택자는 지정된 요소의 자손인 모든 요소에 매치됨

#### Child Selector
자식 선택기는 지정된 요소의 자식인 모든 요소를 선택함

#### Adjacent Sibling Selector 
인접한 형제 선택자는 다른 특정 요소 바로 뒤에있는 요소를 선택하는데 사용됨  
인접한 형제 선택자는 동일한 부모요소를 가져야함

#### General Sibling Selector 
일반 형제 선택자는 지정된 요소의 다음 형제인 모든 요소를 선택함