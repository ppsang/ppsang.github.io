---
title: hexo环境及跳坑
date: 2017-05-24 23:23:09
category: [前端]
tags: [js hexo]
---
### 记录下安装hexo的过程中遇到的问题以及踩过的坑
<p>偶然间看到hexo+github教程，是个轻量级的博客，可以自己定制显示的各种样式，感觉比较高大上，于是乎就按照教程进行安装，但是安装的过程应该来说并不怎么顺利，所以就记录一下我在安装的过程中所遇到的问题
</p>
<!-- more -->
### 安装过程
- 前提条件：
 - 需要安装[node.js](http://nodejs.cn)环境
 - 需要有一个[github](https://github.com)账号
- 安装Hexo
```
  sudo npm install -g hexo
```
- 初始化一个hexo项目
```
  新建一个文件夹，用来存放要写的文章，并在命令行里面进入这个文件夹
  hexo init 初始化项目
  hexo generate (简写 hexo g) 根据初始化的hello-word.md生成静态html文件
  hexo server (简写 hexo s) 在本地4000端口启动服务，访问http://localhost:4000 或者 http://127.0.0.1:4000 预览项目
```
  - 【注】如果输入hexo s出现端口占用错误
  ```
   ps -ef | grep hexo 查看被4000占用的端口，找到占用的线程号
   kill -9 “占用的线程号” 关掉占用4000端口的程序
   hexo s 重新启动程序
  ```

### 更换主题
- 现在可以在本地预览生成的博客的大致样子，但是默认的主题比较丑，所以需要去网上下载我们比较喜欢的主题


### 期间遇到的问题
- 当使用hexo d时可能会遇到 ERROR Deployer not found: git 或者 ERROR Deployer not found: github
 - 解决方法： npm install hexo-deployer-git --save
