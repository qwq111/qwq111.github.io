---
title: 如何恢复静态hexo
logoIcon: fa-cube
---
### 如何将本地hexo备份上github ###
>+ 前提：已经配置密匙且上传过hexo静态页面
``` 
$ git clone "远程仓库地址"
```
>+ 先将远程仓库克隆到本地，
>+ 然后进入clone的目录，打开git bash
```
$ git checkout -b hexo  
```
>+ 创建并切换成hexo目录
>+ 然后将本地博客内的东西全部复制到该目录中
>+ 然后删除theme目录下的所有.git文件
```
$ git add --all
```
>+ 该命令将所有文件加入缓存区
```
$ git commit "源代码"
```
>+ 该命令将文件添加 自述内容
```
$ git push origin hexo 
```
>+ 推送至远程仓库
### 如何重新恢复本地博客 ###
>+ 前提：已下载git和nodejs 和绑定密匙
>+ 先找一个文件用来准备存放需要克隆的文件
>+ 在该目录下打开git bash界面
```
$ git clone -b hexo "远程仓库地址"
```
>+ 然后打开该文件，输入
``` 
npm install hexo --save
```
>+ 然后就完成了，接下来操作与正常hexo上传相似，
>建议以后每次操作为（前提是如果在本地预览后没有问题，）。

``` 
$ git pull
$ hexo d -g
$ git add -all
$ git commit -m "代码自述"
$ git push -u origin hexo
```
