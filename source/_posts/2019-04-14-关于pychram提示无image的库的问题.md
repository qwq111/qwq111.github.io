---
title: 关于pychram提示无image的库的问题
layout: post
---
> 使用media库时提示**No module named Image**，为了安装media模块，首先安装了numpy，pygame，pygrighics，以及PIL，以及ampy等模块.
> 结果提示这个错误信息，花了三天时间，终于看到了大佬的博客，茅塞顿开，
> + **解决方法为将所有import Image的地方全部替换为from PIL import Image**