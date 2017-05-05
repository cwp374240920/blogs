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

### ubuntu下的安装：
    
    sudo apt-get install thefuck

然后在你的bash/fish/zsh中，设置别名(alias)，即在你的.bashrc/.zshrc中添加这样一行：

    eval "$(thefuck --alias)"

就可以使用了。

#### 小小的尝试一下：

