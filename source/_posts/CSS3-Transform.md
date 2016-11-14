---
title: CSS3 Transform
date: 2016-11-10 09:45:26
tags: [css3,前端]
---
一个简单模仿时间表的旋转例子.
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Demo</title>
</head>
<style>
.box{
 position:absolute;
 left: 50%;
}
.box .second{
  width: 2px;
  height: 50px;
  background-color: #999;
  animation:to-rotate 1s linear infinite;
  -webkit-animation:to-rotate 1s linear infinite;
  -moz-animation:to-rotate 1s linear infinite;
  -ms-animation:to-rotate 1s linear infinite;
}
.box .minute{
  width: 2px;
  height: 30px;
  background-color: #000;
  position: absolute;
  top:20px;
  animation:to-rotate 10s linear infinite;
  -webkit-animation:to-rotate 10s linear infinite;
  -moz-animation:to-rotate 10s linear infinite;
  -ms-animation:to-rotate 10s linear infinite;
}
@-webkit-keyframes to-rotate{
  0%{-webkit-transform:rotate(0deg);-webkit-transform-origin:bottom center;}
  50%{-webkit-transform:rotate(180deg);-webkit-transform-origin:bottom center;}
  100%{-webkit-transform:rotate(360deg);-webkit-transform-origin:bottom center;}
}
@-moz-keyframes to-rotate{
  0%{-moz-transform:rotate(0deg);-moz-transform-origin:bottom center;}
  50%{-moz-transform:rotate(180deg);-moz-transform-origin:bottom center;}
  100%{-moz-transform:rotate(360deg);-moz-transform-origin:bottom center;}
}
@-ms-keyframes to-rotate{
  0%{-ms-transform:rotate(0deg);-ms-transform-origin:bottom center;}
  50%{-ms-transform:rotate(180deg);-ms-transform-origin:bottom center;}
  100%{-ms-transform:rotate(360deg);-ms-transform-origin:bottom center;}
}
@keyframes to-rotate{
  0%{transform:rotate(0deg);transform-origin:bottom center;}
  50%{transform:rotate(180deg);transform-origin:bottom center;}
  100%{transform:rotate(360deg);transform-origin:bottom center;}
}
</style>
<body>
<div class="box">
  <div class="minute"></div>
  <div class="second"></div>
</div>
</body>
</html>
```

```
Internet Explorer 10、Firefox、Opera 支持 transform 属性。
Internet Explorer 9 支持替代的 -ms-transform 属性（仅适用于 2D 转换）。
Safari 和 Chrome 支持替代的 -webkit-transform 属性（3D 和 2D 转换）。
Opera 只支持 2D 转换。
```

[官方文档](http://www.w3school.com.cn/cssref/pr_transform.asp)

### 2D transform常用的transform-function的功能:
* translate()：用来移动元素，可以根据X轴和Ｙ轴坐标重新定位元素位置。在此基础上有两个扩展函数：translateX()和translateY()。
* scale()：用来缩小或放大元素，可以使用元素尺寸发生变化。在此基础上有两个扩展函数：scaleX()和scaleY()。
* rotate()：用来旋转元素。
* skew()：用来让元素倾斜。在此基础上有两个扩展函数：skewX()和skewY()。
* matrix()：定义矩阵变形，基于X轴和Y轴坐标重新定位元素位置。

### 3D transform常用的transform-function的功能:

* translate3d()：移元素元素，用来指定一个3D变形移动位移量
* translate()：指定3Ｄ位移在Ｚ轴的位移量。
* scale3d()：用来缩放一个元素。
* scaleZ():指定Z轴的缩放向量。
* rotate3d()：指定元素具有一个三维旋转的角度。
* rotateX()、rotateY()和rotateZ()：让元素具有一个旋转角度。
* perspective()：指定一个透视投影矩阵。
* matrix3d()：定义矩阵变形。

### transform-origin:
* top = top center = center top = 50% 0
* right = right center = center right = 100%或(100% 50%)
* bottom = bottom center = center bottom = 50% 100%
* left = left center = center left = 0或(0 50%)
* center = center center = 50%或（50% 50%）
* top left = left top = 0 0
* right top = top right = 100% 0
* bottom right = right bottom = 100% 100%
* bottom left = left bottom = 0 100%
