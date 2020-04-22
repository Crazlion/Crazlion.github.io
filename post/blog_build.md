---
title: "hugo + github page 搭建自己的博客"
date: 2020-04-22T17:43:24+08:00
draft: true
categories: ["hugo"]
---
搭建自己的博客完善自己的知识体系
## windows本地搭建
#### 1、下载hugo

直接访问官网：https://gohugo.io/  
本来打算在ubuntu的虚拟机搭的，但是直接下载的版本有点低，和后面的主题有点不兼容，可能我用的是阿里云的apt-get源  
所以直接下载[windows的0.61版本](https://github.com/gohugoio/hugo/releases/download/v0.61.0/hugo_0.61.0_Windows-64bit.zip)  
把hugo.exe拷贝到一个PATH目录下，感觉这样省事，之前设置过
#### 2、验证安装
``` shell
hugo version
Hugo Static Site Generator v0.57.2-A849CB2D windows/amd64 BuildDate: 2019-08-17T17:54:13Z
```

#### 3、创建站点
找一个目录，打开命令行
``` shell
hugo new site blog
```  

#### 4、下载主题
因为现在还是一个空的站点，没有index.html，即使现在起也是一个空的
使用的一个简单主题[maupassant](https://github.com/flysnow-org/maupassant-hugo)  
```
cd themes
git clone https://github.com/flysnow-org/maupassant-hugo.git maupassant
```
修改config.toml
```
languageCode = "zh-cn"
title = "Crazy lion's blog"
theme = "maupassant"
```

#### 5、创建一个blog
这个主题有一个规定文档要放在post目录下
```
hugo new post/my-first-post.md
```

#### 6、启动服务
```
hugo server -D
```
打开浏览器查看http://localhost:1313/