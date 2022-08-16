### CSS 구문
```
h1 {color : blue; font-size: 12px;}
↑      ↑      ↑ 
선택자 속성    값
``` 

### CSS 선택자 종류
1. 요소 선택
```
p {
	~~
}
```

2. id 선택
```
#para1 {
	~~
}
```

3. 클래스 선택
```
.center {
	~~
}
```

4. 범용 선택
```
* {
    ~~
}
```

5. 그룹화 선택
```
h1, h2, p {
	~~
}
```

### CSS 삽입방법

1. 외부
<head>섹션 내에서 <link>요소 내에서 정의
  
```
<!DOCTYPE html>
<html>
<head>
<link rel="stylesheet" href="mystyle.css">
</head>
<body>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
```
  
2. 내부
<head>섹션 내에서 <style>요소 내에서 정의	
  
```
<!DOCTYPE html>
<html>
<head>
<style>
body {
  background-color: linen;
}

h1 {
  color: maroon;
  margin-left: 40px;
}
</style>
</head>
<body>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
```

3. 인라인
단일 요소에 고유 스타일 적용(권장하지 않음)
```
<!DOCTYPE html>
<html>
<body>

<h1 style="color:blue;text-align:center;">This is a heading</h1>
<p style="color:red;">This is a paragraph.</p>

</body>
</html>
```

여러개의 스타일이 정의되면 마지막으로 읽은 스타일이 적용됨.


### 주석
CSS : /* */  
HTML: <!-- -->

### CSS 색상이름
- tomato
- orange
- dodgerblue...

### 배경색 바꾸기
style="background-color: [colorName]";

### 글자색 바꾸기
style="color : [colorName];"

### Border 색 바꾸기
style="border: []px solid [colorName];"

### 색 설정값
RGB, HEX, HSL, RGBA, HSLA 사용가능

#### rgb(red, green, blue)
0 ~ 255까지

#### rgba(red, green, blue, alpha)
rgb에서 투명도(alpha)추가 0.0 ~ 1.0까지

#### hex
#rrggbb
줄여서 #rgb로도 가능
#ff00cc -> #f0c

#### hsl
hsl(hue, saturation, lightness)
색조, 채도, 밝기  
색조는 0 ~ 360까지 0은 빨간색, 120은 녹색, 240은 파란색  
채도는 0 ~ 100%까지  
밝기는 0 ~ 100%까지

#### hsla
hsl(hue, saturation, lightness, alpha)

### CSS 배경

#### 배경색
background-color : [colorName];

##### 투명도
opacity : 0.0;
0.0 ~ 1.0까지 값이 낮을수록 투명해짐

rgba로도 가능

#### 배경 이미지
background-image: url("[url]");

#### 배경 반복
기본적인 background-image 속성은 이미지를 가로 및 세로로 반복함.

background-repeat: repeat-x; 가로로 반복  
background-repeat: repeat-y; 세로로 반복  
background-repeat: no-repeat; 반복 없음  

#### 배경 위치
background-position: [position]

#### 배경 부착
배경 이미지가 스크롤되어야 하는지 고정되어야하는지를 지정  
backgorund-attachment: fixed; 고정  
background-attachment: scroll; 스크롤

#### 약식 속성
하나의 단일 속성에 모든 배경 속성 지정가능
before
```
body {
  background-color: #ffffff;
  background-image: url("img_tree.png");
  background-repeat: no-repeat;
  background-position: right top;
}
```
after
```
body {
  background: #ffffff url("img_tree.png") no-repeat right top;
}
```

약식 속성을 사용할때 순서
background-color  
background-image  
background-repeat  
background-attachment  
background-position  

### CSS border 스타일
border-style 속성으로 테두리 종류를 지정할 수 있음
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

groove, ridge, inset, outset의 효과는 border-color의 색상을 따름

![image](https://user-images.githubusercontent.com/32587845/184806389-0ab5f4b6-ed74-4717-8ec5-89dc04ebb005.png)

### CSS border 폭
border-width로 테두리 폭을 정할 수 있음
px, pt, cm, em 등으로 설정하거나 
thin, medium, thick으로 설정할 수 있음

border-width 속성은 4가지 값을 가짐(top, right, bottom, left 시계방향)

 ### CSS border 색상
 border-color 속성으로 테두리 색상을 정함
 - name
 - hex
 - rgb
 - hsl
 - transparent

 4가지 값(top, right, bottom, left)에 각각 색 지정가능

### CSS border 각각의 면
border-top-style - 위
border-right-style - 오른쪽
border-bottom-style - 아래
border-left-style - 왼쪽

### CSS border 약식 속성
border-width  
border-style(필수)  
border-color  
순으로 지정됨

한쪽 면만 적용가능
border-bottom: 6px solid red;

### CSS border 둥글게
border-radius: []px;

### CSS 마진
border 외부의 공간을 만드는데 사용

개별
margin-top  
margin-right  
margin-bottom  
margin-left  

약식
margin-top  
margin-right  
margin-bottom  
margin-left  
순으로 지정

margin에 3가지 값이 있는경우  
margin: 25px 50px 75px;  
-> top 25, right left 50, bottom 75  

margin에 2가지 값이 있는경우
margin: 25px 50px;
-> top bottom 25, right left 50

#### auto
margin 속성을 auto로 사용해서 element를 가로로 가운데에 맞출 수 있음  
element는 지정된 너비를 차지하고 나머지 공간이 왼쪽과 오른쪽 여백 사이에 균등하게 분할됨

#### 상속
값으로 inherit를 사용하면 부모 element의 마진을 상속받아서 사용

#### 마진 축소
두개의 여백이 하나의 여백으로 축소되는 경우가 있음
상단 및 하단의 여백 -> 가장 큰 여백과 동일하게 축소됨
아래 여백(50px) + 상단 여백(20px)이면 합쳐서 70px이 될것같지만
가장 큰 여백인 50px로 나옴.

### CSS 패딩
패딩은 테두리 내부의 element 주위에 공간을 만드는데 사용

개별
padding-top
padding-right
padding-bottom
padding-left

약식
마진과 동일

#### 패딩 및 element 너비
width로 지정된 너비에서 패딩을 주면 element의 전체 너비에 추가된다.   
```
div {
	width: 300px;
	padding: 25px;
}

너비가 300? -> 300px + 왼쪽 패딩 + 오른쪽 패딩 = 350px
```   
패딩과 관계없이 너비를 유지하려면 box-sizing 속성을 사용

### CSS 높이, 너비, 최대 너비
height: 높이
width: 너비

높이와 너비 속성에는 패딩, 테두리, 여백이 포함되지 않음.

가질 수 있는 값
- auto: 기본값, 브라우저가 높이 너비 계산 
- length: px, cm 등의 높이/너비 정의
- %: 높이/너비를 백분율로 정의
- initial: 높이/너비를 기본값으로 설정
- inherit: 높이/너비를 부모 값 상속

#### 최대 너비 설정
max-width 속성으로 element의 최대 너비를 설정할 수 있음
100%로 설정하면 요소의 기본 크기 이상으로 조절되지 않음

### CSS box model
margin, border, padding, content로 구성

#### 요소의 너비와 높이
전체 요소 너비 = 너비 + 왼쪽 패딩 + 오른쪽 패딩 + 왼쪽 테두리 + 오른쪽 테두리 + 왼쪽 여백 + 오른쪽 여백

전체 요소 높이 = 높이 + 상단 패딩 + 하단 패딩 + 상단 테두리 + 하단 테두리 + 상단 여백 + 하단 여백

next -> https://www.w3schools.com/css/css_outline.asp