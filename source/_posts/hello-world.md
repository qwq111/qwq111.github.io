---
title: 如何搭建hexo博客
logoIcon: fa-cube
---
个人认为用来搭建博客[hexo](https://hexo.io/zh-cn/)比其他的简单,加之借鉴了各位大神的博客，来记录一下自己搭hexo博客的经历 **平台为github** 

### 初篇
>+ 需要自己先下载好[git](https://git-scm.com/downloads)和[npm](https://nodejs.org/en/download/)工具,然后注册一个github账号.
>+ [git](https://blog.csdn.net/buknow/article/details/80325986)和[npm](https://www.cnblogs.com/goldlong/p/8027997.html)安装教程
### 安装hexo

>[安装教程](https://runindark.com/2019/03/23/My)
##  用hexo上传博客及如何用git上传源码 ##
### 保存源码 ###
>+ 完成此步骤需要先配置github密匙。
>+ 克隆远程仓库下来
```
$ git clone "项目地址"
```
>+ 克隆下来后，打开下载下来的文件，然后删除除.git之外的所有文件
>+ 找到自己建立的本地博客文件，将其全部复制进入仓库文件。
>+ 然后新建分支并切换,已经建立的可以跳过此步
```
$ git checkout -b "hexo"
```
>+ 然后就会会显示当前已进入这个分支
>+ 然后将输入下面代码将博客文件添加入缓存区
```
$ git add --all 
```
>+ 输入下面代码，添加文件自述
```
$ git commit -m "自述内容"
```
>+ 提交至远程仓库hexo分支
```
$ git push -u origin hexo -f
```
>+ -f表示强制命令
>+ 至此，源文件上传完成，哪怕换了一个环境也能复制下来继续写博客，每次上传博客都执行一下上面三步。
### 上传博客 ###
>+ 上面的步骤只是保存源文件，但是想要显示页面还不行。上传博客执行下面三步走
```
$ hexo s
```
>+ s就是server，可以启动本地服务器，进行预览
```
$ hexo g
```
>+ 生成静态页面
```
$ hexo d
```
>+ 上传页面