---
title: 如何配置github项目密匙
logoIcon: fa-cube
---
## 前言 ##
>在此之前需要先要拥有一个自己的GitHub账号;
以及已经安装了git工具
## 操作 ##
>+ 首先找到自己的./ssh文件（有些可能找不到那也也是正常的，因为.ssh文件并不是初始化系统必虚的，该目录用于保存生成过的密匙匙，随便找个地方打开git bash，执行下面操作也有效）
>+ 右击.ssh文件夹打开git bash窗口，在打开的git bash窗口里，输入下面信息
```
$ ssh-keygen -t rsa -C "youemail"
```
>+ 解释一下，youemail需要换成自己的注册GitHub账号的邮箱;然后在第一个提示句输入自己的github用户名_rsa ;*(可以换成其他的，这个用户名以后就是你的登陆句柄 )*

>+ 这个时候.ssh文件就已经建立了，在c盘的用户下面可以找到它，然后在这个文件里面打开git bash窗口（已经到打开过了可以跳过）

>+ 然后继续在窗口内输入（一定要检查路径是不是在.ssh下，不然会很麻烦，ps-不堪回首）然后输入下面这句
```
$ touch coufig
```
>+ 然后打开coufig文件输入以下内容，注意不要在语句前加缩进和空格（ps-不堪回首）下面的one用于代替我的用户名
```
# one
Host one.github.com
HostName github.com
PreferredAuthentications publickey
IdentityFile ~/.ssh/one_rsa
User one
```
>+ 注意不要改动 （详细参考[博客](https://www.cnblogs.com/xjnotxj/p/5845574.html?tdsourcetag=s_pcqq_aiomsg)
>+ 前面弄完，并且已经保存后，执行下一步操作。
## 添加公匙 ##
>+ 打开自己的github账号，并且在设置里面的ssh里面添加ssh，密匙名字随便写，内容就要在.ssh文件里面找到自己建立的--比如我的是one_rsa.pub，将里面的内容复制到上面就行
>+ 然后就是最后一步，测试
```
$ssh -T git@one.github.com
```
>+ 注意，我上面的one仅是样例，可以更改，可以与多个github绑定，设置不同的句柄，每个新账号的添加步骤一致。

如果不知道路径在哪 请参考大佬[博客](https://runindark.com/2019/03/23/My%20first%20blog/)