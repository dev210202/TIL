### CSS Image Gallery
이미지 갤러리를 생성하는 방법
```
<!DOCTYPE html>
<html>
<head>
<style>
div.gallery {
  margin: 5px;
  border: 1px solid #ccc;
  float: left;
  width: 180px;
}

div.gallery:hover {
  border: 1px solid #777;
}

div.gallery img {
  width: 100%;
  height: auto;
}

div.desc {
  padding: 15px;
  text-align: center;
}
</style>
</head>
<body>

<div class="gallery">
  <a target="_blank" href="img_5terre.jpg">
    <img src="img_5terre.jpg" alt="Cinque Terre" width="600" height="400">
  </a>
  <div class="desc">Add a description of the image here</div>
</div>

<div class="gallery">
  <a target="_blank" href="img_forest.jpg">
    <img src="img_forest.jpg" alt="Forest" width="600" height="400">
  </a>
  <div class="desc">Add a description of the image here</div>
</div>

<div class="gallery">
  <a target="_blank" href="img_lights.jpg">
    <img src="img_lights.jpg" alt="Northern Lights" width="600" height="400">
  </a>
  <div class="desc">Add a description of the image here</div>
</div>

<div class="gallery">
  <a target="_blank" href="img_mountains.jpg">
    <img src="img_mountains.jpg" alt="Mountains" width="600" height="400">
  </a>
  <div class="desc">Add a description of the image here</div>
</div>

</body>
</html>
```

### CSS Image Sprites
image sprite는 단일 이미지에 넣은 이미지 모음을 뜻함.  
이미지가 많은 웹페이지는 로드할때 오래걸리고 여러 서버요청을 생성할 수 있음. 이미지 스프라이트를 사용하면 서버 요청수가 줄어들고 대역폭이 절약됨

#### Image Sprites - Simple Example
세개의 개별 이미지를 사용하는 대신 단일 이미지를 사용  
CSS를 사용해서 필요한 이미지의 일부만 표시할 수 있음

#### Image Sprites - Create a Navigation List
navigation list를 사용하기 위해 스프라이트 이미지를 사용하고 html 리스트를 사용해서 배경이미지와 링크를 지원

#### Image Sprites - Hover Effect
이미지가 여러개의 개별 이미지가 아닌 하나기때문에 hover를 사용해도 로딩이 없음 