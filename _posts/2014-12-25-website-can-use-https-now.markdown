---
author: hxl
comments: true
date: 2014-12-25 09:38:09+00:00
layout: post
slug: website-can-use-https-now
title: 网站开通了Https方式访问
tagline: website-can-use-https-now
wordpress_id: 124
categories:
- web
- 技术之路
tags:
- 网站
---
*注：这里说的网站，是指我的Wordpress站*  
20141228更新：网站已经全面启用Https方式访问，现在，网站将默认使用SSL/TLS。同时，网站的FTP服务器也已经启用了FTPS，大家可以通过FTPS://www.xn--vqq397gs70a.cn 访问。（20150525：现在网站的FTP服务器暂时关闭了。）  

在调试了好几天、换了N个系统版本和镜像后，网站终于是开通了Https访问。现在，通过https://www.何相龙.cn 就可以使用Https方式访问本站了。  
备注：现在网站更换了域名，请使用[https://tec.hxlxz.com](https://tec.hxlxz.com)。（20150525）  
首先，什么是Https呢？  
简单地说，Https就是加密后的Http，这种访问方式保证了你与本站的通信是保密的（不能被第三人窃取或篡改）。  
如果想继续了解Https SSL/TLS，以下这些能帮到你  
[维基百科](https://zh.wikipedia.org/wiki/%E8%B6%85%E6%96%87%E6%9C%AC%E4%BC%A0%E8%BE%93%E5%AE%89%E5%85%A8%E5%8D%8F%E8%AE%AE)　[百度百科 ](http://baike.baidu.com/link?url=3F1JbqbH0ncLLHcEO8R16w67YP5qIshgp0rQtWGcfWsLQan0xLSc7NzLHRTosSPOW4IqrIZrKrGEZh1e1VDMBq)　[果壳网](http://www.guokr.com/post/114121/)  
本人暂时才疏学浅，无力从理论上来介绍这个东西。  
个人认为，Https在很大程度上能代替Http，是Http的升级。现在Google等互联网巨头已经全面支持Https，由于个人对加密的热爱，我就搭建了这样一个Https的访问方式。  
好，废话不说，我是这样搭建的。  
1. 申请SSL证书，我是在wosign.com申请的免费SSL证书，对于我们来说，免费的就够了（壕请无视这句）。申请过程就不再赘述了。个人建议用SHA-2的算法。  
2. 因为我的网站上有多个域名需要开通Https访问，而传统的SSL只支持一个IP绑定一个Https网站。所以，我在查阅资料后找到了一种叫SNI的方法，以达到我的需求（具体可以看[这里](http://www.ttlsa.com/web/sni-multi-domain-virtual-host-ssl-tls-authentication/)）。  
3. 上述文章并没有介绍IIS的SNI设置方法，而我的网站上采用IIS架设的，于是，我又以“IIS SNI”作为关键词，进行了搜索，找到了[这篇文章](http://iis75europeanhosting.hostforlife.eu/post/European-IIS-8-Hosting-Amsterdam-IIS-8-Server-Name-Indication.aspx)。  
4. 由于只有IIS8才支持SNI，而IIS8只能安装在win2012上，于是我把刚从win2003换到win2008的服务器又换为了win2012。这中间还出来个小插曲，在云主机上装好win2012后，我的数据盘无法挂载。于是，提交工单给工程师解决，经过4个小时的努力，搞定了，我也因此获得了100倍赔偿（15天服务器续期）。  
5. 设置，成功。  
关于如何架设网站。。。Google去！我是采用的[phpStudy](http://www.phpstudy.net/)这款软件加上IIS8来搭建的。  
大概就这样了，按照以前的方法，本来需要一个多域名SSL证书；提供SNI，就可以使用多个免费的证书来实现单IP上多个网站或域名的Https访问。  
这篇文章供大家参考吧。  

[![知识共享许可协议](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-nc-sa/4.0/)  
网站开通了Https方式访问 由 [何相龙]() 创作，采用 [知识共享 署名-非商业性使用-相同方式共享 4.0 国际 许可协议](http://creativecommons.org/licenses/by-nc-sa/4.0/)进行许可。  
[在Wordpress站上浏览本文](https://tec.hxlxz.com/?p=124)
