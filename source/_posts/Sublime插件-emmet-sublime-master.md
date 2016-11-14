---
title: 'Sublime插件[emmet-sublime-master]'
date: 2016-11-07 14:19:55
tags: 随笔
---
## 符号
 * '>:表示嵌套的元素
  `nav>ul>li` -> `<nav><ul><li></li></ul></nav>`
 * +:同级标签符号
  `div+div+p ` -> ` <div></div><div></div><p></p>`
 * #:id属性 标签默认div
  `#header` -> ` <div id="header"></div>`
 * . :class属性 标签默认div
  `.header ` -> ` <div class="header"></div>`
 * ^:可以使该符号前的标签提升一行
 ` div>p>span+span^^a ` -> ` <div><p><span></span><span></span></p></div><a></a>`
 * ():  一组元素
  `div>(header>ul>li*2>a)+footer>p ` -> ` <div> <header> <ul> <li><a href=""></a></li> <li><a href=""></a></li> </ul> </header> <footer> <p></p> </footer> </div>`
 * $: 多个元素循环变量
   `ul>li.item$*3 ` -> ` <ul> <li class="item1"></li> <li class="item2"></li> <li class="item3"></li></ul>`
 * []:元素属性符号
   `a[href=#] ` -> ` <a href="#"></a>`
 * {}:元素标签里的值
   `a{click}` -> ` <a>click</a>`
## 文本文档：
 * html:5 或!：用于HTML5文档类型
 * html:xt：用于XHTML过渡文档类型
 * html:4s：用于HTML4严格文档类型

## CSS 缩写:
 * p 表示%
 * e 表示 em
 * x 表示 ex

## 循环标签使用
### ul>li.item$*5
```
<ul>
 <li class="item1"></li>
 <li class="item2"></li>
 <li class="item3"></li>
 <li class="item4"></li>
 <li class="item5"></li>
 </ul>
```
### h$[title=item$]{Header $}*3
```
<h1 title="item1">Header 1</h1>
<h2 title="item2">Header 2</h2> 
<h3 title="item3">Header 3</h3>
```
### ul>li.item$$$*5
```
<ul> 
  <li class="item001"></li>
  <li class="item002"></li> 
  <li class="item003"></li> 
  <li class="item004"></li> 
  <li class="item005"></li> 
</ul>
```
### ul>li.item$@-*5
```
<ul>
<li class="item5"></li>
<li class="item4"></li>
<li class="item3"></li>
<li class="item2"></li>
<li class="item1"></li>
</ul>
```
### ul>li.item$@3*5
```
<ul>
  <li class="item3"></li>
  <li class="item4"></li> 
  <li class="item5"></li>
  <li class="item6"></li>
  <li class="item7"></li>
</ul>
```