---
title: CSS3 box-reflect镜像
date: 2016-11-10 14:44:09
tags: [css3,前端]
---
box-reflect的一个小例子
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Demo</title>
</head>
<style type="text/css">
.reflect img{
  -webkit-box-reflect:below 2px -webkit-linear-gradient(transparent,transparent 50%,rgba(255,255,255,.3));
  -moz-box-reflect:below 2px -moz-linear-gradient(transparent,transparent 50%,rgba(255,255,255,.3));
  -ms-box-reflect:below 2px -ms-linear-gradient(transparent,transparent 50%,rgba(255,255,255,.3));
  -o-box-reflect:below 2px -o-linear-gradient(transparent,transparent 50%,rgba(255,255,255,.3));
  box-reflect:below 2px linear-gradient(transparent,transparent 50%,rgba(255,255,255,.3));
}
.reflect div{
  -webkit-box-reflect:below 2px -webkit-linear-gradient(transparent,transparent 50%,rgba(255,255,255,.3));
  -moz-box-reflect:below 2px -moz-linear-gradient(transparent,transparent 50%,rgba(255,255,255,.3));
  -ms-box-reflect:below 2px -ms-linear-gradient(transparent,transparent 50%,rgba(255,255,255,.3));
  -o-box-reflect:below 2px -o-linear-gradient(transparent,transparent 50%,rgba(255,255,255,.3));
  box-reflect:below 2px linear-gradient(transparent,transparent 50%,rgba(255,255,255,.3));
  font-size: 30px;
  font-weight: 600;
}
</style>
<body>
<div class="reflect">
  <img src="./test.jpg" alt="">
  <div>有倒影</div>
</div>
</body>
</html>
```

### box-reflect参数
```
box-reflect:<direction>|<offset>|<mask-box-image> 镜像位置|偏移|遮罩
box-reflect: none #无镜像
box-reflect: above||below||left||right  #映射在对象上边||下边||左边||右边
box-reflect: above 1px //添加倒影并向下位移1像素,可用负数可使用百分比
box-reflect: above 1px linear-gradient(transparent,transparent 50%,rgba(255,255,255,.3) #添加倒影
<mask-box-image>参数:
url：使用绝对或相对地址指定遮罩图像。
linear-gradient：使用线性渐变创建遮罩图像。
radial-gradient：使用径向(放射性)渐变创建遮罩图像。
repeating-linear-gradient：使用重复的线性渐变创建背遮罩像。
repeating-radial-gradient：使用重复的径向(放射性)渐变创建遮罩图像。

```


### 注意
* 行内元素不支持镜像,行内元素使用镜像需设置display属性
* IE6-10不支持
* Firefox 4.0-9.0不支持
