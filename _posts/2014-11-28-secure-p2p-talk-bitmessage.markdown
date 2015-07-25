---
author: hxl
comments: true
date: 2014-11-28 11:39:52+00:00
layout: post
slug: secure-p2p-talk-bitmessage
tagline: secure-p2p-talk-bitmessage
title: 加密的P2P即时通讯软件——比特信使用指南
wordpress_id: 21
categories:
- 杂谈
tags:
- 加密
- 安全
- 开源
- 软件介绍
---
 
众所周知，现有的大部分的即时通讯软件和电子邮箱都是中心化的，而且大部分软件不能有效地加密。今天，我将介绍一种加密的、去中心化的P2P技术通信软件——比特信（Bit-message）。   

## 一、下载与运行
在https://bitmessage.org/wiki/Main_Page 下载相应版本的比特信，双击下载的文件即可运行比特信。如果出现安全警告，请选择允许。  
[![btx (1)](https://tec.hxlxz.com/wp-content/uploads/2014/08/btx-1-1024x563.png)](https://tec.hxlxz.com/wp-content/uploads/2014/08/btx-1.png)   

## 二、第一次运行
[![btx (2)](https://tec.hxlxz.com/wp-content/uploads/2014/08/btx-2.png)](https://tec.hxlxz.com/wp-content/uploads/2014/08/btx-2.png)
这是比特信的主界面，如果没有特殊情况，请选择现在连接。  
要正常地使用比特信，你需要创建地址。切换到“您的身份”选项卡  
[![btx (3)](https://tec.hxlxz.com/wp-content/uploads/2014/08/btx-3.png)](https://tec.hxlxz.com/wp-content/uploads/2014/08/btx-3.png)  
如果网络状态正常，界面的右下角的红色圆形应该已经变为黄色或绿色，表示已经正常连接比特信网络。  
点击左上角的新建按钮。  
[![btx (4)](https://tec.hxlxz.com/wp-content/uploads/2014/08/btx-4.png)](https://tec.hxlxz.com/wp-content/uploads/2014/08/btx-4.png)  
这里提供两种创建方式：随机数创建或密钥生成。随机数创建的地址的安全性稍高于密钥创建的地址，但密钥创建的地址在特殊情况下可以使用密钥进行恢复。我个人建议新手使用密钥创建。  
1、使用随机数创建  
没有什么多说的，直接点击“OK”就行了  
2、使用密钥创建  
**输入一个独特的、不容易被猜到的、足够长的字符串作为你的密钥，请不要使用生日、名字、证件号码或书名、诗句、简单的单词句子作为你的密钥！**  
记住下图红线标出的数据和你的密钥。  
**警告：掌握了上述数据和密钥，就掌握了你的地址！请注意保密。**  
[![btx (5)](https://tec.hxlxz.com/wp-content/uploads/2014/08/btx-5.png)](https://tec.hxlxz.com/wp-content/uploads/2014/08/btx-5.png)   
默认，会生成8个地址，现在把这些地址给你的好友，他们就可以通过比特信给你发信息了！
[![btx (6)](https://tec.hxlxz.com/wp-content/uploads/2014/08/btx-6.png)](https://tec.hxlxz.com/wp-content/uploads/2014/08/btx-6.png)   

## 三、发送消息
[![btx (7)](https://tec.hxlxz.com/wp-content/uploads/2014/08/btx-7.png)](https://tec.hxlxz.com/wp-content/uploads/2014/08/btx-7.png)  
在“1”处选择一个你的地址作为发送地址  
在“2”处输入或粘贴你想发送消息到的地址  
在“3”处输入消息  
无误后，点击“4”发送  
[![btx (8)](https://tec.hxlxz.com/wp-content/uploads/2014/08/btx-8.png)](https://tec.hxlxz.com/wp-content/uploads/2014/08/btx-8.png)  
在“已发送”选项卡，可以看到正在做工来发送消息。  
为什么要做工呢？  
其实这个是为了防止垃圾信息造成的网络阻塞，是一种工作量证明机制（POW），提供进行一定量的hash运算，向网络证明了这条消息在发生前已经做了功。对于正常的消息来说，这种做工机制没有太大影响（大概半分钟吧），但是对于恶意的网络攻击者来说，做工是无法避免的，这就设置了足够的障碍来保护网络。   
[![btx (9)](https://tec.hxlxz.com/wp-content/uploads/2014/08/btx-9.png)](https://tec.hxlxz.com/wp-content/uploads/2014/08/btx-9.png)   
可以看到，我的消息已经发生成功，等待回执了。  
[![btx (10)](https://tec.hxlxz.com/wp-content/uploads/2014/08/btx-10.png)](https://tec.hxlxz.com/wp-content/uploads/2014/08/btx-10.png)  
这是对方收到消息后的显示  

## 四、接收消息
其实很简单，打开比特信，在收件箱界面就可以看到你的消息。  

## 五、其他
其实，比特信的功能很强大，上述内容只是基本的应用，如果大家有兴趣，可以深入研究，也欢迎一起讨论、交流！我的比特信地址是BM-2cSmerJ4BMg5z8kvtKJqixUAyuDsZXnLJT

[![知识共享许可协议](https://i.creativecommons.org/l/by-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-sa/4.0/)  
加密的P2P即时通讯软件——比特信使用指南 由 [何相龙]() 创作，采用 [知识共享 署名-相同方式共享 4.0 国际 许可协议](http://creativecommons.org/licenses/by-sa/4.0/)进行许可。  
[在Wordpress站上浏览本文](https://tec.hxlxz.com/?p=21)