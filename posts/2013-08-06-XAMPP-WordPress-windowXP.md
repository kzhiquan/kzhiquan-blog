---
layout: post
title: "XAMPP-Wordpress-WindowXP"
date: 2013-08-06 21:25:14
comments: true
categories: literal
---


## XAMPP 安装配置 ##
1. apache + mysql + php 环境的安装配置；下载XAMPP：http://www.apachefriends.org/en/index.html；
2. 安装 XAMPP到D:\xampp，在D:\xampp中找到xampp-control.exe打开，在XAMPP Control Panel Application中启动 Apache 和 Mysql 服务；
3. 打开本地数据库管理界面：http://localhost/phpmyadmin/， 创建数据库wordpress.


## 安装配置 Wordpress ##
1. 下载最新版的 WordPress:http://wordpress.org/latest.zip，解压并存放在 D:\xampp\htdocs 目录下。
2. 在浏览器中打开http://localhost/wordpress/，数据库用户名为root, 密码为空；
3. 完成相关配置，如主题，用户名/密码；
4. 打开http://localhost/wordpress/即可访问前端页面， 打开http://localhost/wordpress/wp-admin/访问后端页面；