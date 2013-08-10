---
layout: post
title: "mongodb-install-WindowXP"
date: 2013-03-10 21:25:14
comments: true
categories: literal
---

##安装 配置 过程##

1. 下载安装包：官方下载地址:http://www.mongodb.org/downloads,选择正确的版本；
2. 新建目录"D:\MongoDB"，解压下载到的安装包，找到bin目录下面全部.exe文件，拷
   贝到刚"D:\MongoDB"目录下；
3. 在"D:\MongoDB"目录下新建"data"文件夹，它将会作为数据存放的根文件夹；
4. 设置环境变量，我的电脑->高级->环境变量设置,在用户变量PATH，系统变量Path中增加D:\MongoDB,重新启用命令行即可使用；


## 配置Mong服务器端 ##

打开CMD窗口,配置成功会显示27017,28017端口正在监听；
> mongod --dbpath D:\MongoDB\data


## 客户端工具 ##

1. 使用RockMongo:MongoDB可视化管理工具；
2. 下载地址：http://code.google.com/p/rock-php/downloads/list 中的rockmongo-
            on-windows-v0.0.2.rar；
3. 解压，双击运行rockstart.bat会自动运行如下页面；
4. 用户名和密码登录，默认为"admin"和"admin"；