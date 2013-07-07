---
layout: post
title: "折腾博客小记"
date: 2012-11-29 23:43:00
comments: true
categories: computer technology
---
慢慢地屈从于现实，从原先的坚持前端HTML/CSS/JS，后端C++，数据库sqlite的自主开发小型博客的模式，
到现在的wordpress，自己只开发主题的形式，拿来的主义胜苦涩的理想主义，只因张嘴巴要吃饭，不管怎样，
曾经理想过。

自主开发博客，暂且叫<a href="https://github.com/kzhiquan/blog-eyesee" target="_blank">eyesee</a>吧，
只是一个雏形，是一个基于linux平台的epoll事件机制开发的，一个主线程实现网路数据的收发， HTTP协议解析，
另一个主线程实现任务的调度分配， 其他线程池中的线程实现业务逻辑，与SQLITE数据库交互，JSON数据格式的转化等；
其优点是具有多流水线处理的模式，非常快速，不会阻塞，代码量小，部署方便。存在的缺憾是，如果用进程来处理网路数据的收发和任务的调度，
则系统更加稳定；线程池未设计好，只实现了一个简单的存储线程对象的地方，并未实现释放；无锁的消息队列未实现，
特别是系统对消息的处理有点乱。缺憾很多，本来想就做一件事情，把它做好，才去开发这个的，但是三四个月过去了，
雏形出来了，后面就苦涩了。不过，也是一种锻炼吧，自我阿Q下，源码公开于<a href="https://github.com/kzhiquan/blog-eyesee" target="_blank">GITHUB</a>，
欢迎大家拍砖。

关于wordpress，最近花了点时间看了下它前端的源码，初一看，太庞大了，臃肿啊，
看着看着，真有种想死的感觉，结构化程序设计为基础，缺少整体上的面向对象设计，
虽然现在PHP开始支持、并鼓励面向对象的设计风格了，但是PHP历史上对类是不支持的。
不过，每天坚持一点点，看着看着，也就习惯了，从初始化参数设置，到数据查询，到数据渲染到前端的过程，
其中包括主题theme下模版的加载，wordpress的缓存Cache机制，wordpress的回调函数机制(add_filter, apply_filter)，
wordpress的widgets机制(注册，调用)，wordpress的层级元素遍历机制(walker, walker_page)等，慢慢找到了路线，
但是一想到单单请求这样一个页面，wordpress就要走完这样一个过程，也真够辛苦的，效率上肯定有影响，虽然有Cache的存在。
对于wordpress，一开始比较疑惑：简单的内容，怎么有这么丰富的表现形式。现在有点明白了，
其一：wordpress的数据是固定的，定制化借助style.css表现，这里要根据wordpress生成的class/ID来编制CSS规则，
或者自己增加class/ID渲染；其二：如果想改变数据或者增加功能，应用插件机制，即add_filter/apply_filter。目前理解到这个水平。

实践了下，编制了一个主题(<a href="https://github.com/kzhiquan/wp-theme-eyeseenull">eyeseenul</a>l)，
也贡献到github上，就是当前这个博客使用的，非常的简单，就当练手了，呵呵。

本来是一个纯后端C/C++的编程者的，接触web开发，一开始后端也想采用C++/C，并不想深入接触Java/ASP/JSP的东西，
探寻过Wt C++ webkit，并实践了下<a href="https://github.com/kzhiquan/blog-eyesee" target="_blank">eyesee</a>， 
但是前端采用JS从后台获取数据再显示，这时，爬虫抓取不到数据，google存在抓取AJAX的数据的方法，不过也不是原生的，不是自动分析解析页面上的javascript，
自动获取数据的，这可能是下一代爬虫发展的方向。后来了解了PHP，因为是开源的，其虚拟机Zend也是开源的，但是通过wordpress的源码的解读，
觉得不够优雅，再后来接触了node.js，似乎找到了方向。

知泉/绍兴/2012.11.29