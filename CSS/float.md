### CSS Layout - float and clear
float 속성으로 요소를 띄울 수 있음  
clear 속성은 지워진 요소 옆과 어느쪽에 떠있을지 지정

#### the float property
float 속성은 콘텐츠의 위치를 지정하고 서식을 지정하는데 사용함  
다음 값을 가질 수 있음
- left
- right
- none (기본값)
- inherit (부모값 상속)

#### the clear property
float 속성을 사용한 다음 요소를 원할 때 clear 속성을 사용함  
float 속성 다음에 요소가 어떤 일이 발생해야하는지 지정.  
다음 값을 가질 수 있음
- none (기본값)
- left
- right
- both (왼쪽 및 오른쪽 아래)
- inherit (부모 상속)

float을 지울때 clear도 마찬가지로 일치시켜야한다.

#### the clearfix hack
float된 요소가 컨테이너 요소보다 크면 overflow가 발생한다.  
clearfix hack을 사용해서 이를 해결 할 수 있음
```
.clearfix {
  overflow: auto;
}
```
clearfix overflow:auto도 작동하지만 새로운 clearfix hack은 사용하기에 더 안전하고 대부분의 웹페이지에 사용됨
```
.clearfix::after {
  content: "";
  clear: both;
  display: table;
}
```


### CSS Layout - Float Examples

#### Grid of Boxes / Equal Width Boxes
float 속성을 사용해서 나란히 띄울 수 있음

각각의 박스에 너비를 늘리는 패딩 또는 테두리를 추가하면 박스가 깨지게 되는데 box-sizing을 사용해서 상자의 전체너비에 패딩과 테두리를 포함하여 박스가 유지되고 깨지지 않음.

#### Equal Height Boxes
같은 높이를 만들기 위해 고정 높이를 설정하는 방법이 있음.  
하지만 유연하지 않음. 항상 같은 양의 내용물이 들어있다고 보장할 수 없음
그래서 CSS3 FlexBox를 사용

#### Navigation Menu
flaot로 하이퍼링크 목록과 가로 메뉴를 만들 수 있음
