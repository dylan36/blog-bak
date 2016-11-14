---
title: Hexo
date: 2016-11-07 13:57:31
tags: 随笔
---
安装
`sudo npm install -g hexo`
初始化
`hexo init`
生成静态页面
`hexo generate`
本地预览
`hexo server`

```
与git建立关联
vim _config.yml 文本最后
deploy:
  type: git
  repo: https://github.com/dylan36/dylan36.github.io
  branch: master

```
`npm install hexo-deployer-git --save`

`hexo clean `
`hexo generate`
`hexo deploy`
`hexo new "title"`