---
author: hxl
comments: true
date: 2015-08-07 16:31:37+00:00
layout: post
slug: android-in-csharp
title: C# 安卓环境搭建记
tagline: android-in-csharp
wordpress_id: 941
categories:
- 技术之路
- 移动端软件
tags:
- 软件
---

早就听说C#可以写安卓程序了，打算试试。  
在VS里建立了一个安卓项目，按提示下载安装xamarin，安装报错。  
[![报错1](https://tec.hxlxz.com/wp-content/uploads/2015/08/android1.png)](https://tec.hxlxz.com/wp-content/uploads/2015/08/android1-433x300.png)  
于是，按提示安装jdk1.6，更新android sdk。  
更新SDK的过程中，尝试开启全局代理，再次安装，安装正常，但是提示要下载SDK，果断退出，等待SDK更新完成。    
过程不多说，尼玛下了一天，最后还是没能搞定。不过好在深夜里网络不错，Xamarin的自动安装程序终于能正常工作了。    
在VS重建个项目，使用自动的仿真器运行，正常；但是尝试在手机上运行，报错。  
[![报错2](https://tec.hxlxz.com/wp-content/uploads/2015/08/android2.png)](https://tec.hxlxz.com/wp-content/uploads/2015/08/android2.png)  
Could not create the Android package. See the Output (Build) window for more details.  
MonoDroid does not support running the previous version.  Please ensure your solution builds before running or debugging it.  
网上有人说要在项目设置中勾选“use shared runtime”，然而我勾上后并没有效果，仍然报错。  
查看日志发现。。竟然是空间不足给闹的。。抢夺到一定也不萌的妹纸的手机来测试。。。然后就没问题了。。。  
然而，虽然仿真调试时没问题了，但是，生成APK的按钮是灰色的，没法点击。于是在网上搜索破解教程。（实在没钱啊。。）  
突然发现C盘被撑爆了。。看来是得去换个大点的固态硬盘了。。检查发现，NDK被装到了我的文档里面，随移动到E盘，并修改环境变量；然后按VS给的提示，修改NDK路径设置。发现昨天下载的临时目录在C:\Users\用户名\AppData\Local\Temp\Xamarin，清除。  
继续来破解。。按照一篇文章的方法搞了搞，然后发现虽然能正常使用，但是会报错。  
[![报错3](https://tec.hxlxz.com/wp-content/uploads/2015/08/android3.png)](https://tec.hxlxz.com/wp-content/uploads/2015/08/android3-485x300.png)  
一番搜索、尝试无效。于是放弃，恢复原状，重新寻找方案。  
于是。。按照另一篇的方法，搞定了。本想写写。。不过太简单，Google去吧。  
虽然破解成功了。。但是。。尼玛，publish android app 这个选项还是灰色的，按不了。。坑死了。。  
在中文网站没有找到解决方案，只好去看看英文的。。没想到一下就找到了，需要取消“use shared runtime”的选择。  
尝试生成，新建密钥，生成和发现样例程序竟然有30M，简直不能忍。搜索得知需要切换到Release模式，切换后，4M，算勉强能接受吧。具体参见[这篇文章](http://www.cnblogs.com/aphason/p/3929887.html)。  

既然安卓的环境都搭建好了，我觉得不能浪费这个跨平台编程工具，觉得把IOS的环境也搭建好。由于IOS的模拟器只能在MAC OSX上运行，然而作为矮穷挫的我没有高富帅专用MAC，只好在虚拟机上安装一个。我使用的是VirtualBox虚拟机。  
开始试了网上的一些方法，安装过程中均提示系统崩溃，没法用，后来按一篇教程，下载了Lion的安装包，并关闭了EFI，终于进入了安装界面。  
使用磁盘工具进行分区，然后继续安装。然后，又卡住了。  
Systrm uptime in nanoceconds：242.。。。。。  
重启，花屏。移除虚拟光盘后再重启。错误如图。
[![报错4](https://tec.hxlxz.com/wp-content/uploads/2015/08/macos1.png)](https://tec.hxlxz.com/wp-content/uploads/2015/08/macos1-453x300.png)  
突然记起那个文件包里面还有个ISO文件，应该是引导文件，于是，挂载上，尝试启动。正常启动。  
然后按照提示在MAC OS上安装xamarin.ios，在vs里尝试连接，提示版本太久。猜测是win端没有安装ios的开发环境。然而发现猜错了。。提示中明明白白写着是build server too old。。看来安装在MAC上的东西老了。。  
在官网上看了好久，没有发现更新的版本，于是猜测是不是MAC的系统版本太老，检查了下，的确不是最新版的，于是，使用系统设置里面的软件更新，重启3次，安装完所有更新后，发现系统并没有被更新。猜测可能在APP Store内更新，检查发现的确如此，尝试更新，提示系统Apple ID，创建帐户，验证邮箱，能成功登录。但是进行更新时，提示当前系统版本不支持银联，让我更新系统。。我去。。我这不就是在更新吗。。。在帐户设置中，把付款方式改为银行卡，终于能够开始更新系统了。  
在等更新的过程中，解决了鼠标滚轮的效果与习惯的不一样的问题，在系统设置-鼠标中，取消“滚动或导航时，使内容按照手指方向移动”的勾选。  
然而更新老是失败。。  

然后，最近事多，暂时搁置一阵（也有可能IOS端不搞了，再说吧）。  
<a href="http://creativecommons.org/licenses/by-nc-sa/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" alt="知识共享许可协议" /></a>  
C# 安卓环境搭建记 由 <a href="https://tec.hxlxz.com/?p=941"   rel="cc:attributionURL">何相龙</a> 创作，采用 <a href="http://creativecommons.org/licenses/by-nc-sa/4.0/" rel="license">知识共享 署名-非商业性使用-相同方式共享 4.0 国际 许可协议</a>进行许可。  
[在Wordpress站上浏览本文](https://tec.hxlxz.com/?p=941)