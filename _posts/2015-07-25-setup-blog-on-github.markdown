---
author: admin_hxl
comments: true
date: 2015-07-25 16:31:37+00:00
layout: post
slug: setup-blog-on-github
title: GitHub博客搭建记
tagline: setup-blog-on-github
wordpress_id: 922
categories:
- 杂谈
---

突发奇想，打算把博客在GitHub上搞个分站，于是说干就干。  
按照[GitHub的官方指南](https://pages.github.com/)，建立好了hxl9654.github.io的项目，并添加了CNAME文件。  
然后又按照[官方教程](https://help.github.com/articles/using-jekyll-with-pages/)，[安装Ruby环境](https://www.ruby-lang.org/en/downloads/)。  
然而，突然发现那个是linux下的教程。。googel得到Jekyll[官方教程](http://jekyll-windows.juthilo.com/1-ruby-and-devkit/)。[Jekyll在windows下的安装方法](http://jekyll-windows.juthilo.com/1-ruby-and-devkit/)。  
[下载安装rubyinstaller](http://rubyinstaller.org/downloads/)，和Ruby DevKit。
在下一步：gem install jekyll时，又被伟大的某Q给搞了。搜索得到，在cmd运行这个指令可以设置CMD的代理：  
{% highlight c %}
set http_proxy=http://proxy.yourname.com:8080
{% endhighlight %}
于是，继续安装。大概10分钟后。。终于装好了。  
然后安装、设置语法高亮。在创建博客时遇到了麻烦，我以为目录需要去配置，但是，搜索无果。  尝试后发现，只要cd到想要的目录就可以了。  
然而jekyll serve后，程序只是建立了一个_site文件夹，然后把CNAME和index.html复制进去了。。这根说好的不一样啊。  
尝试jektll new blog，成功建立blog文件夹，并包含全套文件。复制一下，jekyll serve，完成。  
然后我就把.git文件夹搞不见了。。重新clone。。。  
然后。。搞了好久。。决定放弃，另寻他路。  
搜索发现[这个项目](http://jekyllbootstrap.com/)。简直太爽，直接fork，各种配置说明很详细、简单。就是默认的项目明要改了，不是username.github.com而是username.github.io。  
配置过程中没啥大问题，几个点说说吧：  

1. 留言和追踪就别想了，方校长秒杀之
2. googleapi没得搞。。。换镜像吧。具体是在include文件夹里面的几个文件需要修改。  

其他没啥要说的，就是今晚网速太坑。  

现在博客已经搭建了一个雏形。[在这里](https://hxl9654.github.io/)  

然后就是从wordpress导出xml，转换成markdown格式，以便导入。使用了[exitwp](https://github.com/thomasf/exitwp)。  
按照方法，在windows下尝试，失败。于是使用了kali进行。不要问我为什么不用ubuntu。。  
成功转换后，开始修改格式。本来这一步应该很简单的，但是由于我在写wordpress时不喜欢用&lt;p&gt;标签，导致需要自己修正很多换行问题。主要遇到两个问题  

1. 标题和块不听话，尝试后，发现#和>需要之前有个换行才行。
2. 代码语法高亮导致Jekyll崩溃，搜索和尝试安装运行环境   

找到[这篇文章](http://cn.yizeng.me/2013/05/10/setup-jekyll-on-windows/)，但是尝试操作后发现没有效果。不过，在故障排除第3点描述的错误信息与我类似，说是PATH变量的问题。于是，尝试将已经添加进用户变量PATH中的python目录复制到系统变量，问题解决。    
迁移完文章，可以收工了。  
做几个笔记吧  
内部链接：{百分号 post_url 文件名 百分号}  
如：{百分号 post_url 2014-12-01-list-of-valid-errors 百分号}  
语法高亮：{百分号 highlight 语言百分号}{百分号 endhighlight 百分号}  
如：{百分号 highlight c 百分号}printf("hello world");{百分号 endhighlight 百分号}  

[![知识共享许可协议](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-nc-sa/4.0/)  
GitHub博客搭建记 由 [何相龙]() 创作，采用 [知识共享 署名-非商业性使用-相同方式共享 4.0 国际 许可协议](http://creativecommons.org/licenses/by-nc-sa/4.0/)进行许可。  
[在Wordpress站上浏览本文](https://tec.hxlxz.com/?p=922)