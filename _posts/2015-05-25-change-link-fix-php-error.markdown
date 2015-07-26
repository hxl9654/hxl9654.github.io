---
author: hxl
comments: true
date: 2015-05-25 18:33:22+00:00
excerpt: '想到之前修改网站链接形式的想法，花了一天时间修改本站的链接格式，遇到了一些困难，最终成功。'
layout: post
slug: change-link-fix-php-error
title: 更改了网站的链接形式，改正了PHP配置错误
tagline: change-link-fix-php-error
wordpress_id: 712
categories:
- web
tags:
- web
---

今天，没啥事做，突然想到之前修改网站链接形式的想法，加上打开后台的“分类目录”设置项会跳转到文章的404页面。决定进行一些修改。  
之前我的链接是这样的/p=%post_id%---%year%-%monthnum%-%day%  
例如https://tec.hxlxz.com/p=123---2015-01-01  
这样的链接中，日期似乎并没有什么用，于是，我打算修改成文章ID+标题的形式，是这样的/%post_id%_%postname%  
例如https://tec.hxlxz.com/712_change-link-fix-php-error  
这样一来，链接就直观得多，而且对搜索引擎更友好。  
说做就做，我先到wordpress的设置选项中修改了修改选项。  
[![2015-05-25T14-22-57.974Z](https://tec.hxlxz.com/wp-content/uploads/2015/05/2015-05-25T14-22-57.974Z.png)](https://tec.hxlxz.com/wp-content/uploads/2015/05/2015-05-25T14-22-57.974Z.png)  
然后发现这样并不行，打开文章会报404错误。之前在网上看到，固定链接中带有中文字符在部分平台上会造成404错误，于是，每篇文章挨个改。。。  
爽爆的修改之后，发现Google收录的链接全是老链接，而且点击这些链接全部报404错误。  
唉我去，这样搞，Google会打死我的。  
又一番搜索，发现一款叫permalink finder的插件能解决这个问题（这插件装上就能用，不用改配置）。  
简单地说，当请求的页面不存在的时候，这个插件会自动根据URL的参数来进行文章匹配，然后301重定向到对应的文章。  
但是，经过后来的测试，发现这样做并不能很好地重定向分类目录，这个放在后面再说。  
但是，实际使用时，发现后台有跳转成功的记录，但前台返回500错误，我顿时就呵呵了。插件更新500，登陆500，网络卡还是500，各种500是要闹哪样？  
我又想起了之前看的另一篇文章，说可以禁用PHP的错误提示。于是，禁用了，还是乱码500。  
之前，由于乱码问题，已经修改了各种错误提示页面模板，加上了UTF-8的语言标记。这次，我重新去检查了一下，发现但是肯定是没睡醒，这引号都没配对：  
之前是 
{% highlight html %}
<meta http-equiv="Content-Type" content="text/html; charset="UTF-8"/>
{% endhighlight %}
现在改为 
{% highlight html %}
<meta http-equiv="Content-Type" content="text/html"   charset="UTF-8"/>
{% endhighlight %}
这样，500错误再也不乱码了。  

[![之前傲娇的500](https://tec.hxlxz.com/wp-content/uploads/2015/05/2015-05-25T14-43-60.324Z.png)](https://tec.hxlxz.com/wp-content/uploads/2015/05/2015-05-25T14-43-60.324Z.png)  

> 之前傲娇的500  

[![现在的样子。（为了看一个正常的500错误，我容易吗我。。。）](https://tec.hxlxz.com/wp-content/uploads/2015/05/2015-05-25T14-43-59.324Z.png)](https://tec.hxlxz.com/wp-content/uploads/2015/05/2015-05-25T14-43-59.324Z.png)  

> 现在的样子。（为了看一个正常的500错误，我容易吗我。。。）  

但是，500错误仍然出现（只是变得正常的500了，不乱码了）  
我在IIS配置里，打开了详细错误信息显示。发现错误报告里一堆E_Warning。我去，原来是这个原因导致的500频发啊。  
试着修改php.ini文件，发现修改这个的还是有些难度的。于是用PHP.ini的模板文件php.ini-production覆盖了当前文件，一刷新，发现又呵呵了，这个文件默认没有打开mysql相关的扩展，wordpress报错。  
于是，打开php.ini，去掉相关模块引用语句的注释标记（就是前面的分行），重启IIS，再次尝试。发现PHP再次报错：FastCGI溢出。由于没有遇到过这个问题，我进行了搜索，得到了答案：  没有配置扩展的目录。在php.ini中查找了下，去掉了当前系统（win）的扩展目录的配置语句的注释符号。  
这下总算成功了，302跳转正常，再也没有坑爹的500错误了。没想到这次改链接还修复了之前困然我很久的500问题。现在想来，应该是我当时错用了php的开发模式配置文件php.ini-development（也有可能phpstudy的默认配置就是这个）。  
但是，现在还有个问题：打开后台的“分类目录”设置项，仍然报404错误。之前我尝试着删除web.config（这个文件里有URL重写的配置，这样能使用伪静态），删除后，访问“分类目录”设置项正常。  
我仔细检查web.config的配置语句，发现其中写到，有关键字“tag”的，交给index.php处理。初步判断问题就在这里了，尝试删除这条设置，问题解决。但是，这样一来，针对标签的伪静态配置就失效了，标签功能无法正常使用。于是，修改标签和分类的前缀，完美地解决了问题。至此，网站上的链接配置算是完成了。  
现在还要解决Google搜索到的分类目录的重定向问题。  
正在打算解决这个问题的时候，喜闻乐见的事情发生了，之前那个插件开始抽风，无奈之下，选择使用redirection来手动配置301重定向。大概半个小时搞定了，幸好博客的东西还不多，否则得累死（也是东西多的话，得另外找办法了吧。。）  
现在的状态是，Google是出来几个带有中文的链接不能正确重定向之外，其他的都搞定了。那几个中文的，就放那里吧，等Google自己删掉吧。  
本来打算添加个长文章分页的功能，不过按照网上的办法，始终没能成功。  
[http://codex.wordpress.org.cn/Function_Reference/wp_link_pages](http://codex.wordpress.org.cn/Function_Reference/wp_link_pages)  
大概是要在需要分页的地方插入<!-–nextpage–->标签，然后在主题的single.php文件的<?php the_content(''); ?>后面添加<?php wp_link_pages(); ?>  
找了好久都没找到single.php里的the_content，然后，看到了另一篇文章，说这个函数可能在其他文件里面。于是，有一番寻找，终于有了发现，找到了这个函数。但是这个函数的后面已经有wp_link_pages了。尝试着再加一次或者替换原函数，没有任何效果。于是，我彻底晕了，完全不明白为什么文章的分页没有显示出来。  
好的，本人已经成功累死，睡觉去了。  

参考资料：  
[https://codex.wordpress.org/zh-cn:%E4%BD%BF%E7%94%A8%E5%9B%BA%E5%AE%9A%E9%93%BE%E6%8E%A5](https://codex.wordpress.org/zh-cn:%E4%BD%BF%E7%94%A8%E5%9B%BA%E5%AE%9A%E9%93%BE%E6%8E%A5)  


[![知识共享许可协议](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-nc-sa/4.0/)  
更改了网站的链接形式，改正了PHP配置错误 由 [何相龙]() 创作，采用 [知识共享 署名-非商业性使用-相同方式共享 4.0 国际 许可协议](http://creativecommons.org/licenses/by-nc-sa/4.0/)进行许可。  
[在Wordpress站上浏览本文](https://tec.hxlxz.com/?p=712)