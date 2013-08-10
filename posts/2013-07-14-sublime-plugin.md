---
layout: post
title: "sublime2-plugin/sublime2-插件"
date: 2013-03-10 21:25:14
comments: true
categories: literal
---

## 安装Package Control 插件的方法 ##

1. 打开sublime2;
2. 按下Control + `, 调用Console;
3. 将以下代码粘进命令行中并回车;
	import urllib2,os;pf='Package Control.sublime-package';ipp=sublime.installed_packages_path();os.makedirs(ipp) if not os.path.exists(ipp) else None;open(os.path.join(ipp,pf),'wb').write(urllib2.urlopen('http://sublime.wbond.net/'+pf.replace(' ','%20')).read())

4. 重启 Sublime2 Text，如果在 Preferences -> Package Settings中见到Package Control这一项，就说明安装成功了;


## markdown preview ##

1. sublime2 text 中编辑的 markdown 语法可以在浏览器中显示;
2. shift+commad+p -> markdown preview:preview in browser;

## terminal ##
1. open termianl on current file or root project;

