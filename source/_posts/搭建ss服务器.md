---
title: 搭建ss服务器
date: 2017-05-28 11:23:28
category: [其他]
tags: [Shadowsockets 翻墙 ss]
---
<blockquote style="text-align: center;">
是时候大步向前了
</blockquote>

<p>搭建vpn和ss服务器都能够实现翻墙的效果，但是ss服务器在客户端里面能够设置自动代理模式，可以很方便的实现访问国内国外网站两不误,所以只是翻墙的化，搭建一个ss服务器还是一个不错的选择</p>
### 步骤
<!-- more -->
- 首先需要一个在国外的服务器(废话)
    - 使用ssh登录 ssh root@ip地址，输入密码登录(win下可以下载putty或者使用gitbash,mac直接使用终端就好了)
- 安装pip环境：
```
    yum install python-setuptools && easy_install pip
```
- 安装 shadowsocks       
```
    pip install shadowsocks
```
- 安装完毕是不是很简单
- 启动
```
    ssserver -p 8888(要使用的端口号) -k password(自定义的密码) -m rc4-md5
```
- 现在就可以在客户端进行配置了，如果连接成功，会在命令行内打印连接的日志，比如访问的网站信息，注意必须要在服务器的安全组规则里面开放这个端口(如：阿里云服务器，默认只开启了22端口，需要手动添加要开放的端口)
- 停止命令
```
    sudo ssserver -d stop
```
- 现在ss服务器是在前台启动的，现在进行配置下，使他在后台运行
- 创建一个配置文件
```
    touch /etc/shadowsocks.json
```
- 编辑文件
```
    vim /etc/shadowsocks.json
    输入内容：
    {
        "server":"my_server_ip",
        "server_port":8888(自定义的端口号),
        "local_address": "127.0.0.1",
        "local_port":1080,
        "password":"mypassword(自定义连接的密码)",
        "timeout":300,
        "method":"aes-256-cfb"
    }
```
- 最后一步 后台启动
```
    ssserver -c /etc/shadowsocks.json --user nobody -d start
```
- linux常用的命令
```
    ps -ef | grep shadowscokets # 查看指定的软件的运行情况
    kill -9 '线程号' # 杀死指定线程
```
### 特别感谢:
- [SS+digital Ocean搭建教程](http://www.kevinandhu.com/?page_id=43)
- [git 官方文档](https://github.com/shadowsocks/shadowsocks/wiki/Shadowsocks-%E4%BD%BF%E7%94%A8%E8%AF%B4%E6%98%8E)

  前人栽树，后人乘凉，感谢他们的贡献！

###### ps 翻墙后可测试留言
