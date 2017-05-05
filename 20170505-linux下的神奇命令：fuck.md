---
title: Linux下的神奇命令：fuck
date: 2017-05-05 17:44:59
tags:
---
# Linux下的神奇命令：fuck

今天刷微信公众号的时候发现一个蛮有意思的文章，说的是linux下的一个很有意思的命令：fuck，具体怎么好玩看接下来的图就知道了。
![](http://mmbiz.qpic.cn/mmbiz_gif/9aPYe0E1fb1XqUgmjsKhtHl5icxG3gqXzwrN021cLHyEbxHcCn51JfSMsjkMYWIcjkJFZhDIyJhIsw5p2Wm94Ww/0?wx_fmt=gif&tp=webp&wxfrom=5&wx_lazy=1)
怎么样，是不是很有趣？

其实这个命令来自一款应用：thefuck，是用来修复在命令行中上一条错误的命令。这款应用下载了几千次，在 GitHub 上有很多 star，并有几十个优秀的贡献者。

## ubuntu下的安装：
    
    sudo apt-get install thefuck

然后在你的bash/fish/zsh中，设置别名(alias)，即在你的.bashrc/.zshrc中添加这样一行：

    eval "$(thefuck --alias)"

就可以使用了。

## 小小的尝试一下：

比如我想输入

    sudo apt-get install vim 

我故意输错：

    aptget install vim

试试:

![](https://github.com/cwp374240920/blogs/blob/master/pics/fuck%5D.png?raw=true)

经过一遍遍fuck调教，最终终于输入正确了自己想要的命令:sudo apt-get install vim

也可以想象到，当时的开发者肯定每次终端中输入错误命令的时候，内心大喊一声fuck，然后动手写了这么个应用。真是既有用又有趣。

自己也尝试一下吧～

