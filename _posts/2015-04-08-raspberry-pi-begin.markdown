---
author: hxl
comments: true
date: 2015-04-08 02:53:18+00:00
layout: post
slug: raspberry-pi-begin
title: 树莓派初调记
tagline: raspberry-pi-begin
wordpress_id: 351
categories:
- 单片机
- 技术之路
tags:
- 树莓派
- 硬件
- 软件
---

最近，瑞狐拍卖板子，搞到块radxa，结果发现不怎么好用，主要是社区资源太少，只好退掉，入手了块树莓派。  
顺丰快递就是快，前一天下单，第二天就收到了，除了树莓派之外，我还搞了些配件，壳子、VGA线、散热器之类的。  
下面上点图  
[![树莓派外壳](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG_20150401_155635.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG_20150401_155635.jpg)  

> 树莓派外壳  

[![配件全家福](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG_20150401_155743.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG_20150401_155743.jpg)  

> 配件全家福  

[![拆开外壳后的东西](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG_20150401_155820.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG_20150401_155820.jpg)  

> 拆开外壳后的东西  

[![树莓派正面](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG_20150401_155833.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG_20150401_155833.jpg)  

> 树莓派正面  

[![树莓派背面](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG_20150401_155847.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG_20150401_155847.jpg)   

> 树莓派背面

[![保护壳](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG_20150401_155931.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG_20150401_155931.jpg)   

> 保护壳  

[![保护壳](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG_20150401_155956.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG_20150401_155956.jpg)  

> 保护壳  

[![装好保护壳的树莓派](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG_20150401_162254.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG_20150401_162254.jpg)  

> 装好保护壳的树莓派  

[![完成！](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG20150408183536.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG20150408183536.jpg)  

> 完成！  

安装过程还好，不怎么难，只是我手贱把外壳给搞坏了一块，试过各种方法都没有搞好，甚至我还用热风枪把壳子融合，试着粘合在一起，结果轻轻一动，又掉下来了。然后。。。  

[![算了，透明胶粘粘吧。。](https://tec.hxlxz.com/wp-content/uploads/2015/04/1429328001251.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/04/1429328001251.jpg)  

> 算了，透明胶粘粘吧。。  

树莓派的系统，其实很好装，在[官方网站的下载页面](https://www.raspberrypi.org/downloads/)下载NOOBS，解压复制进SD卡，插进树莓派，按提示选择系统，安装，也就搞定了。  
至于要重装系统，开机时按shift，也能搞。如果是想完全清除SD卡的话，去[SDCard官网下载SD Formatter](https://www.sdcard.org/downloads/formatter_4/index.html)，然后，安装，选择盘符，搞搞也就行了。注意，千万不要手贱选错盘符。  

[![SDFormatter](https://tec.hxlxz.com/wp-content/uploads/2015/04/SDFormatter.png)](https://tec.hxlxz.com/wp-content/uploads/2015/04/SDFormatter.png)

[![正在装系统](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG_20150401_180930.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG_20150401_180930.jpg)  

> 正在装系统  

[![连接显示器](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG_20150401_180934.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG_20150401_180934.jpg)  

> 连接显示器  

然后就是喜闻乐见地配置各种环境，firefox，中文包，设置时区，设置显示器啥的。我还顺手超了点频。  
[![超了15%的频率吧。打码的是视频解码许可证。](https://tec.hxlxz.com/wp-content/uploads/2015/04/1429333662598.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/04/1429333662598.jpg)  

> 超了15%的频率吧。打码的是视频解码许可证。  

什么？怎么配置环境？别急，马上教你。  
[![有问题，问度娘。度娘傲娇的话，请问谷歌娘](https://tec.hxlxz.com/wp-content/uploads/2015/04/baidu_use.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/04/baidu_use.jpg)  

> 有问题，问度娘。度娘傲娇的话，请问谷歌娘  

总之，搞好了基本的一些操作，再上点图。
[![文件管理器](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG_20150401_184824.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG_20150401_184824.jpg)  

> 文件管理器  

[![试着用python写的hello pi。话说python是树莓派官方推荐的编程语言啊](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG_20150401_202018.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG_20150401_202018.jpg)  

> 试着用python写的hello pi。话说python是树莓派官方推荐的编程语言啊

[![自带的minecraft，不过是阉割版的，只有很少的物品、很小的地图。](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG_20150402_002050.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG_20150402_002050.jpg)  

> 自带的minecraft，不过是阉割版的，只有很少的物品、很小的地图。  

[![C语言编辑环境](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG_20150402_171046.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG_20150402_171046.jpg)  

> C语言编辑环境  

[![不用我说这是什么了吧](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG20150401214439.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG20150401214439.jpg)  

> 不用我说这是什么了吧

[![本来说用小米的无线wifi的，结果各种装不上。](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG20150406201608.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG20150406201608.jpg)  

> 本来说用小米的无线wifi的，结果各种装不上。

[![奇怪的无线网卡，红色的USB口是什么情况？？！！](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG20150406181551.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG20150406181551.jpg)  

> 奇怪的无线网卡，红色的USB口是什么情况？？！！  

[![高清1080P视频无压力啊](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG20150407225937.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/04/IMG20150407225937.jpg)  

> 高清1080P视频无压力啊  
 
顺便一提，要是想用树莓派硬解码播放wmv等格式的视频的话，是需要单独购买许可证的，大概3美刀的样子。在[这里](http://www.raspberrypi.com/)购买许可证。什么？你想软解码？洗洗睡吧，就树莓派的那个CPU，亲测，卡得动都动不了。  
好的，这篇流水帐完成了，有什么问题，欢迎交流。  

[![知识共享许可协议](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-nc-sa/4.0/)    
树莓派初调记 由 [何相龙]() 创作，采用 [知识共享 署名-非商业性使用-相同方式共享 4.0 国际 许可协议](http://creativecommons.org/licenses/by-nc-sa/4.0/)进行许可。  
[在Wordpress站上浏览本文](https://tec.hxlxz.com/?p=351)