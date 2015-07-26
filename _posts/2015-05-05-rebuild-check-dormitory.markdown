---
author: hxl
comments: true
date: 2015-05-05 18:05:54+00:00
layout: post
slug: rebuild-check-dormitory
title: 重新架构了之前的查寝系统
tagline: rebuild-check-dormitory
wordpress_id: 437
categories:
- web
- 技术之路
- 软件
tags:
- web
- 查寝系统
- 软件
- 项目
---

之前搭好了一个学生会的查寝系统，项目日志在[这里](https://tec.hxlxz.com/?p=354)，系统在[这里](http://chaqin.echoiot.com)  
项目现在在[github](https://github.com/hxl9654/chaqin)上开源，欢迎watch、fork。
但是当时写代码十分仓促，没有按照代码书写规范来写，也没有加注释啥的。  
今天，我把这个代码重新架构了，添加了注释，修改了格式，修复了一些不稳定的东西。  
具体来说  

> 增加了文件头注释和语句注释  
> 修改了错误的空格、逗号  
> 修改了错误的代码缩进    
> 将原来使用的用于正常结束程序的die函数换成了exit函数，并在此之前关闭数据库连接  
> 将程序模块化，分成了更多的文件  

到现在为止，这个项目有大概1270行代码（含注释）。  

### 2015年5月7日更新
今天把昨天的版本好好修改了下，修复了很多BUG（因为昨天没有测试）。没想到我的第一个稍微拿得出手的项目竟然是一个说做就做的web项目。  
[把第一个发布版搞出来了，虽然是beta版。](https://github.com/hxl9654/chaqin/releases/tag/v1.0beta)  
也没啥好说的，如果想知道怎么慢慢改的，可以去github的[提交历史](https://github.com/hxl9654/chaqin/commits/master)那里看看。  
[欢迎送星，欢迎围观和fork](https://github.com/hxl9654/chaqin)。  
[![cq1](https://tec.hxlxz.com/wp-content/uploads/2015/05/cq1.png)](https://tec.hxlxz.com/wp-content/uploads/2015/05/cq1.png)  

[![cq2](https://tec.hxlxz.com/wp-content/uploads/2015/05/cq2.png)](https://tec.hxlxz.com/wp-content/uploads/2015/05/cq2.png)  

[![2015-05-08T14-43-21.796Z](https://tec.hxlxz.com/wp-content/uploads/2015/05/2015-05-08T14-43-21.796Z.png)](https://tec.hxlxz.com/wp-content/uploads/2015/05/2015-05-08T14-43-21.796Z.png)  


[![知识共享许可协议](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-nc-sa/4.0/)  
重新架构了之前的查寝系统 由 [何相龙]() 创作，采用 [知识共享 署名-非商业性使用-相同方式共享 4.0 国际 许可协议](http://creativecommons.org/licenses/by-nc-sa/4.0/)进行许可。  
[在Wordpress站上浏览本文](https://tec.hxlxz.com/?p=437)