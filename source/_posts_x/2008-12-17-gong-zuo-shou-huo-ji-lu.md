---
layout: post
status: publish
published: true
title: 工作收获记录
author:
  display_name: 小飞熊
  login: fbbear
  email: fbbear@sina.com
  url: 'https://lfbear.com'
author_login: fbbear
author_email: fbbear@sina.com
author_url: 'https://lfbear.com'
excerpt: 收获
wordpress_id: 57
date: '2008-12-17 15:55:06 +0800'
date_gmt: '2008-12-17 07:55:06 +0800'
categories:
  - 工作心语
tags:
  - 收获
  - 优化
  - web
comments: []
abbrlink: 31439
---
<p>最近公司给我们搞了两次培训，记录一些自己的收获（非培训内容，自己总结的一些东东），否则又被淡忘了~ 欢迎交流（知识都是越交流越多哦）<br />
<!--more--><br />
<strong>Mission 1&nbsp; 高性能的web页面</strong></p>
<p>估计大家都有这种经历，开一个网页，要等上很久，结果出来后是&ldquo;该页无法显示&rdquo;或者只出现了残缺的部分内容。这种体验的确会让用户感觉很不爽，当然导致这种现象的原因很多，可能是客户端的问题，但大多都是服务器端的问题。so，就服务器端的优化说上几点，主要是给前端开发工程师(包括RIA及页面builder)。</p>
<p>1、尽可能的减少http请求，学过网络的人都会知道，http协议是应用层协议，过多的http请求势必会导致过多的tcp/ip连接，而大家都知道，建立一次tcp/ip连接需要三次握手哦，因此减少http请求无疑会减少网络通讯的成本，从而加快了页面载入的速度。</p>
<p>一个html/htm页面应该算作一个http请求，然后页面中的image，flash等元素也会算作一个http请求，如果能够减少不必要的这些元素当然好，但是有时你或许会说，这些都很重要，不能扔掉。ok，既然不能扔掉我们就不要仍嘛，再想其他办法。一个业内经典的优化image的方案：将所有的small images做到一张大图上面，然后用css的定位技术去获取需要的图片，这种方法应该是被很多网站屡试不爽的方法吧。一次http请求搞定所有small images。</p>
<p>2、同样的，减少tcp/ip连接显得更加直接。</p>
<p>a.具体做法是在做http的header传输时应用keep-alive（如服务器端支持）；</p>
<p>b.使用恰当的缓存机制：静态资源可以把缓存时间设置为永不过期，动态资源可以根据需求设置恰当的过期时间。（这里还有一个业内人士经常使用的秘密，静态资源设置为永不过期，但是为静态资源的文件名中加入版本号，例如my.js命名为my_0.1.0.js更加恰当，这样静态资源的更新不会给用户带来不良的体验）</p>
<p>c.使用socket reuse</p>
<p>这个需要根据服务器环境来使用，有兴趣的同学可以google一下（汗，其实偶也了解不多）</p>
<p>d.尽量减少代码用使用的子域名数量（一般控制在4-8个为宜，具体可视访问流量和是否使用负载均衡等因素具体考虑）</p>
<p>3.使用g-zip压缩，使网络上传输压缩数据，这样减少带宽开支，大部分服务器都支持gzip压缩的。当然，也不是说压缩好就到处使用呢~ 推荐使用策略：几K或几十K以上的，由字符构成的文件，如果js、html、xml 等 ，对jpeg使用gzip应该没有什么意思吧</p>
<p>4.css放页首，js放页尾（详见文末资料）</p>
<p>5.均衡负载的时候最好不要使用etags（详见文末资料）</p>
<p>--------------- 并不美丽的分割线 ---------------</p>
<p><strong>Mission&nbsp;2&nbsp; 你的站点到底需要什么</strong></p>
<p>这一节讲的是数据分析。对线上产品进行布码监测，对访问异常采取应对解决方法。这是一个很好的习惯，大型网站可以组织员工进行检测系统的开发，小型网站和个人网站建议使用<a href="http://www.google.cn/analytics/zh-CN/">http://www.google.cn/analytics/zh-CN/</a>&nbsp;这套系统做的真的是很好，可以尝试使用。</p>
<p>目的：使用数据分析的目的很简单，分析谁是你的敌人（恶意访问你资源的人），谁是你的朋友（正常用户），敌人多了怎么办，朋友多了怎么办。敌人多了可能要加强安全性处理，增加安全机制；朋友多了就要增加服务器的部署，CDN等技术来优化用户的使用体验。</p>
<p>还有通过分析的数据也可以对某些时间进行某种预测，如出现突发事件，在特殊时间访问量的变化趋势等。</p>
<p>一句话概括：既要知道你做的是什么，又要知道你做的效果如何；阶段性的用统计的结果和预测信息去优化下一阶段你要做的事情！</p>
<p>--------------- 并不美丽的分割线 ---------------</p>
<p>教程资料下载：<a href="/assets/images/20081226_117427.rar" target="_blank">高性能的Web页面</a></p>