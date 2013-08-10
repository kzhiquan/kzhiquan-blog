---
layout: post
title: "GitHub-SSHKey-WindowXP"
date: 2013-08-07 21:25:14
comments: true
categories: literal
---


## 安装 Git Bash ##

1. 由于windows XP 上没有自带的Git, 需要下载安装 Git Bash, 因此在这里下载了Git-1.8.3-preview20130601；
2. 安装完成以后，直接进命令行运行：
3. >ssh-keygen  一直确定yes下去；
4. 在C:\Documents and Settings\Administrator\.ssh\下产生两个文件：id_rsa和id_rsa.pub；


## 配置Github ##

5. 用记事本打开id_rsa.pub文件，复制内容，在github.com的网站上到ssh密钥管理页面，添加新公钥，随便取个名字，内容粘贴
6. 配置用户名后，就可以git pull, push, clone，与github.com进行通信。
