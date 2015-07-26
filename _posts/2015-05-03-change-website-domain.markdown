---
author: hxl
comments: true
date: 2015-05-03 15:05:22+00:00
layout: post
slug: change-website-domain
title: 网站域名体系改动
tagline: change-website-domain
wordpress_id: 410
categories:
- 杂谈
tags:
- web
- 记事
---
*注：这里指的网站是我的Wordpress站*  
之前我的几个网站分别用了不同的域名,这样每年的域名费用都是一大笔开支,而且几个网站直接看上去也没有关联，加上之前用的.cn的中文域名实在太low。由于我的几个网站也没啥规模，完全算是自己玩玩，所以我决定换个统一的域名来搞所有网站。  
在跟妹子的一番商量后，我们最后选定了hxlxz.com这个域名，含义嘛，自己猜。5位的.com域名，不算太low。为啥说.cn的low呢？百度去，哦，不对，是google去！  
在修改bit站域名时，我很NC地在每篇文章中修改各种链接，大概20分钟搞完了，在搞tec站的时候，我发现，也是还这么NC地慢慢改的话，基本就不用吃晚饭了。  
于是，搜索大法好，在网上搜索后得到以下答案（由于这个结果都烂大街了，再注明是哪里看到的也没啥意义）  
在安装wordpress的数据库中执行以下SQL语句：  

{% highlight sql %}
UPDATE wp_posts SET post_content = replace( post_content, 'OldURL','NewURL') ;  
UPDATE wp_comments SET comment_content = replace(comment_content, 'OldURL', 'NewURL') ;  
UPDATE wp_comments SET comment_author_url = replace(comment_author_url, 'OldURL', 'NewURL');  
{% endhighlight %}

然后，这样搞了搞，发现没效果。突然想到我这个网站的前缀不是 wp_ ，修改后重新执行，搞定。  
接着就是301重定向，google、百度提交域名更换信息啥的，没啥好说的。  
现在我的网站主要有两个  
蜀相比特 [bit.hxlxz.com](http://bit.hxlxz.com)  
蜀相技 [tec.hxlxz.com](https://tec.hxlxz.com)  
我在搞一个新的网站，至于是什么，等我的大招CD好了再说吧。  
这篇文章就这样了。  

[![知识共享许可协议](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-nc-sa/4.0/)  
网站域名体系改动 由 [何相龙]() 创作，采用 [知识共享 署名-非商业性使用-相同方式共享 4.0 国际 许可协议](http://creativecommons.org/licenses/by-nc-sa/4.0/)进行许可。  
[在Wordpress站上浏览本文](https://tec.hxlxz.com/?p=410)