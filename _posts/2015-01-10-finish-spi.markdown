---
author: hxl
comments: true
date: 2015-01-10 17:41:16+00:00
layout: post
slug: finish-spi
title: 搞定了SPI通信
tagline: finish-spi
wordpress_id: 186
categories:
- 单片机
- 技术之路
tags:
- 单片机
- 硬件
- 通信
---

大概在一个多月之前，我就遇到了需要用SPI通信的器件，但是由于51单片机没有提供SPI通信的SFR（似乎有点不严谨，应该说没有提供SPI通信的功能吧），手边也没有现成的教程，加之误以为51单片机驾驭不了SPI这种高端的东西，于是拖延症就发作了。直到昨天，我才由于一款OLED需要用到SPI，终于开始写代码。  
昨天，根据SPI的时序图，很轻松地搞定了SPI主机的发送功能，也没啥好说的。  
今天，同样没花什么力气就搞定了其余的代码，但是运行结果就是不对。不对，还是不对。呵呵。。。
通过逻辑分析仪检查了IO口的电平变化，真没有发现什么错误的地方，倒是很多地方莫名其妙地多加了几（我的测试程序是主机发送一个数到从机，从机加1后发送回主机，主机再加1并发送），随即各种查错，各种无果。  

[![这个是程序调试完成后，逻辑分析仪显示的效果](https://tec.hxlxz.com/wp-content/uploads/2015/01/20150110233617.png)](https://tec.hxlxz.com/wp-content/uploads/2015/01/20150110233617.png)  

>这个是程序调试完成后，逻辑分析仪显示的效果  

最后，发现错误在于我用于保存数据接收结果的局部变量没有初始化，而没有初始化的局部变量是一个随机的值。。。于是。。。这个低级错误就耗费了我一个下午+半个晚上的时间。  
51单片机的SPI函数模块库我已经发布到了FTP服务器了，有需要的可以自行下载。注意，这个函数库是使用GPL许可证授权的。  
好，就这样吧。  
2015-05-25更新：由于FTP服务器关闭，请提供[我的GitHub](https://github.com/hxl9654/C51_Study/tree/master/%E9%9D%9E%E9%87%91%E6%B2%99%E6%BB%A9%E6%95%99%E7%A8%8B/SPI%E4%B8%BB%E6%9C%BA%E6%A8%A1%E5%BC%8F%E6%B5%8B%E8%AF%95)来取得代码。  

[![1420904742940](https://tec.hxlxz.com/wp-content/uploads/2015/01/1420904742940.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/1420904742940.jpg)

[![知识共享许可协议](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-nc-sa/4.0/)  
搞定了SPI通信 由 [何相龙]() 创作，采用 [知识共享 署名-非商业性使用-相同方式共享 4.0 国际 许可协议](http://creativecommons.org/licenses/by-nc-sa/4.0/)进行许可。  
[在Wordpress站上浏览本文](https://tec.hxlxz.com/?p=186)
