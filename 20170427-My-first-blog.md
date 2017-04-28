---
title: 20170427-My-first-blog
date: 2017-04-27 15:44:37
tags:
---
这是我的第一篇博客，就用来记录一下自己怎么搭的hexo环境吧，虽然网上有教程，但自己再理一遍总是有好处的。

### Step 1:nodeJS的安装

首先，安装nodejs。

正如hexo官网最醒目的一句话：A fast, simple & powerful blog framework powered by NodeJS（一个简单快捷又强大的博客框架，由nodeJS提供）所以首先安装nodeJS
在node的[官网](http://nodejs.cn/download/)下载自己需要版本的node，比如我是linux 64位，我就选linux 64位的。
1. 解压node-v6.10.2-linux-x64.tar.xz
    
    xz -d node-v6.10.2-linux-x64.tar.xz
    tar -xvf node-v6.10.2-linux-x64.tar
2. 建立链接

    sudo ln -s your_node_dir/bin/node /usr/local/bin/nodejs
    sudo ln -s your_node_dir/bin/npm /usr/local/bin/npm

注意替换成你自己的node路径

### Step 2:Git的安装
我的是ubuntu 16.04，有git的源，直接apt安装即可
    
    sudo apt-get install git

### Step 3:hexo的安装

使用npm全局安装

    sudo npm install -g hexo-cli                    //hexo命令行
    sudo npm install -g hexo-deployer-git --save    //hexo git端部署器

### Step 4:建立站点

环境搭好了，现在可以搭建站点了。

    hexo init blog//hexo init <站点名>

这条命令执行后，就会在当前目录下建立一个blog名的文件夹

    Blog/
        ├── [1.4K]  _config.yml     //配置文件，具体可以自己查看，待会儿会用到，具体查看官网手册
        ├── [ 174]  db.json
        ├── [ 12K]  node_modules
        ├── [ 448]  package.json
        ├── [4.0K]  source
        └── [4.0K]  themes
    4 directories, 3 files

#### Step 4.1:以本地服务运行

博客初始化成功之后，使用：

    hexo generate//或者可以直接省略成:hexo g
启动本地服务：

    hexo server
然后浏览器里访问http://localhost:4000 就能查看到效果了。

#### Step 4.2:配置到github上

hexo生成的静态页面是要上传到github上面的，所以需要配置好github，首先需要在github上建立一个仓库，仓库名格式是username.github.io，比如我的是cwp374240920.github.io，选右上方的clone or download，复制仓库的ssh地址（也可以是https地址）：比如我的git@github.com:cwp374240920/cwp374240920.github.io.git

在_config.yml文件的最后，把deploy换成自己的值：

    deploy:
    type: git
    repo: git@github.com:cwp374240920/cwp374240920.github.io.git
    branch: master

然后执行deploy

    hexo deploy     //可以简写为：hexo d

这样，hexo就关联好了github，在浏览器里面输入username.github.io，比如我的网址[cwp374240920.github.io](cwp374240920.github.io)就可以访问了。

#### Step 4.3:发表文章

    hexo new "20170427-My-first-blog"   //执行完之后会在:./source/_posts/生成文件名.md结尾的博客，掌握markdown的语法就行，写完再执行接下来的命令
    hexo clean
    hexo generate
    hexo deploy

这样，我的这篇博文就发表出来了并且部署到github服务器上了。

#### Step 4.4:创建一个新的标签页

    hexo new page "new page"
    hexo clean 
    hexo generate 
    hexo deploy

以上就是部署这个标签页在github上的方法。

如果步骤有啥问题，联系我本人：374240920@qq.com，有错误也请指出～