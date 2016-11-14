### 个人博客源备份文件

```
安装Hexo
sudo npm install -g hexo
初始化
hexo init
生成静态页面
hexo generate（hexo g也可以） 
本地启动
hexo server
URL:
http://localhost:4000
---------------------
与git建立关联
编辑 _config.yml
deploy:
     type: git
     repo: https://github.com/dylan36/dylan36.github.io
     branch: master
     
配置完执行
npm install hexo-deployer-git --save
```

### 常用命令
```
hexo clean  
hexo generate
hexo deploy
hexo new "name" 
```
