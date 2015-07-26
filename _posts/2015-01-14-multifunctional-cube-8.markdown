---
author: hxl
comments: true
date: 2015-01-14 18:36:44+00:00
layout: post
slug: multifunctional-cube-8
title: 不务正业的光立方项目日志（8阶全彩多功能光立方）
tagline: multifunctional-cube-8
wordpress_id: 198
categories:
- 单片机
- 技术之路
- 推荐
tags:
- 光立方
- 单片机
- 硬件
- 软件
- 项目
---

寒假了，智能实验室项目被砍了，不高兴。但是那么长的一个月，总得找点事做，正好之前有做光立方的想法，于是就决定做一个8阶全彩的光立方。本日志将持续更新直到项目完成。项目完成后，项目中本人有完全版权的部分，会开源发布在本站的FTP服务器（包括PCB的设计图纸和单片机的程序代码）。好了，废话少说，开工！  


### **2015年1月15日（凌晨）**


今天决定搞8阶全彩的光立方，在实验室的黑板前转悠很久后，我搭建好了设计的基本框架。

[![正在测试全彩LED灯的参数](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150114_195419.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150114_195419.jpg)  

> 正在测试全彩LED灯的参数  

[![第一版构思](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150114_224629.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150114_224629.jpg)  

> 第一版构思  

[![今天的最终设计框架](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150115_005124.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150115_005124.jpg)  

> 今天的最终设计框架  

本来是想搞4阶的光立方的，但是在几个损友的怂恿下，还是最终决定做一个八阶的了。转念一想，八阶的都做了，在加点功能，让它成为一个不务正业的光立方也不错。于是，就有了上图的设计框架。时间也不早了，于是，今天就算结束了。


### **2015年1月16日（凌晨）**


今天，先去查阅了相关数据手册，确定了要使用器件的型号，根据数据手册基本完成了原理图器件库的制作，然后边画PCB原理图边改进、修正设计，也没啥可说的。就是原理图的规模都很庞大，画PCB图的时候不得累死啊。。。唉，看来的确是不作死就不会死啊，慢慢画吧。

[![数据手册君](https://tec.hxlxz.com/wp-content/uploads/2015/01/150116.png)](https://tec.hxlxz.com/wp-content/uploads/2015/01/150116.png)  

> 数据手册君

[![原理图器件库](https://tec.hxlxz.com/wp-content/uploads/2015/01/1501161.png)](https://tec.hxlxz.com/wp-content/uploads/2015/01/1501161.png)  

> 原理图器件库  

[![今天的最终设计框架](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150116_011050.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150116_011050.jpg)  

> 今天的最终设计框架  

[![PCB原理图概览。。。密集恐惧症患者节哀。。。](https://tec.hxlxz.com/wp-content/uploads/2015/01/250116.png)](https://tec.hxlxz.com/wp-content/uploads/2015/01/250116.png)  

> PCB原理图概览。。。密集恐惧症患者节哀。。。

所以。。今天就到这里吧，明天继续。

### **2015年1月18日（凌晨）**

显示器坏了。。。没钱买元件了。。。所以。项目得搁置一段时间了。

### **2015年1月19日（凌晨）**


从今天起，该项目命名为 不务正业的光立方。  
今天又耽搁了，大概修改了下项目方案，然后采购了元器件（别问我上哪搞到的钱），准备正式开工。顺便一提，我还搞了把游标卡尺，用来量器件的封装数据。买两套光立方的配件，整整花了我600大洋啊！支付宝君在哭泣。另一个改进是用小型扬声器代替了原计划的蜂鸣器，一个简单的测试程序表明了这是可行的（话说不用三极管驱动的话，扬声器的声音跟蚊子叫似的。。。）。  

[![扬声器测试板](https://tec.hxlxz.com/wp-content/uploads/2015/01/1423149193342.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/1423149193342.jpg)  

> 扬声器测试板  

我打算将设计中的一些不是很必要的模块用跳线进行连接，以便日后进行功能扩展。基本就是这样，也没干啥事，一天又混过了。。  
再随便一提：TM那个扬声器也太蛋疼了，焊线的时候一不小心烙铁就被吸到上面去了，线也很细，有点容易被焊坏。买LED时，最好多买几十个，免得出现坏的又重新去买。  

[![猜测这是什么](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150119_001357.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150119_001357.jpg)  

> 猜测这是什么  

### **2015年1月20日（凌晨）**


AT24C1024竟然缺货。。。不高兴。。。于是，我们用4个AT24C512替代吧。。。存储容量瞬间×2。  
今天做的事比较杂，继续画原理图，实验了扬声器的电路，实验了光敏电阻的电路，初步测试了驻极体话筒。  
驻极体话筒好麻烦，在声音很大的情况下，输出的电压波动才30mV，还得加放大电路，这个得明天（其实就是今天。。）来实验了。  
光敏电阻测试光强的电路没啥好说的，直接串联个定制电阻接到VCC、GND直接，用AD测试中点对地的电压就成。  
扬声器稍微麻烦点，我的电路图如下，仅供参考：  

[![扬声器电路图](https://tec.hxlxz.com/wp-content/uploads/2015/01/2.png)](https://tec.hxlxz.com/wp-content/uploads/2015/01/2.png)  

> 扬声器电路图  

其他好像没啥好说的了。惯例，放几张图吧。

[![猜](https://tec.hxlxz.com/wp-content/uploads/2015/01/1421686569738.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/1421686569738.jpg)  

> 猜  

[![在测试驻极体话筒](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150120_002200.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150120_002200.jpg)  

> 在测试驻极体话筒  

[![在测试驻极体话筒](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150120_002350.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150120_002350.jpg)  

> 在测试驻极体话筒  

[![在实验扬声器电路](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150119_204241.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150119_204241.jpg)  

> 在实验扬声器电路  

[![目前的PCB原理图。。。你们可以感受下。。。](https://tec.hxlxz.com/wp-content/uploads/2015/01/1.png)](https://tec.hxlxz.com/wp-content/uploads/2015/01/1.png)  

> 目前的PCB原理图。。。你们可以感受下。。。  

好，今天就这样吧。

### **2015年1月22日（凌晨）**


这两天都在弄用驻极体话筒做的环境音量检测模块，大体的思路是用单片机的AD功能检测外部的电压（如下图的Mic点）  

[![我是图](https://tec.hxlxz.com/wp-content/uploads/2015/01/11.png)](https://tec.hxlxz.com/wp-content/uploads/2015/01/11.png)  

> 我是图  

但是刚开始，由于选用的电阻阻值不是很好，通过用手机的最大音量向话筒播放声音，得到的电压波动大概在几十毫伏。对于STC12C5A60S2这款单片机内置的10位AD来说，这个电压变化实在太小了。  
于是，我想放大这个信号，由于在群里的大神说，三极管的线性区域太小，不适合用来放大电压信号，我就放弃了用三极管的想法。我选用了运算放大器这个器件，在网上找了图来制作，可是没有成功，也许是运放需要双电源的原因吧，我的板子只能提供5V的电源（其实3.3V啥的，加个稳压芯片就行，但是运放需要独立的负电压，实在没办法）。  
这里有一点小插曲，当我所以鳄鱼夹线延长示波器的表笔时，示波器总显示一个50Hz的杂波，这是因为环境中有大量的50Hz电磁波（交流市电造成的），而我的鳄鱼夹线并没有屏蔽层，所以就发生了干扰。这个问题困扰了我们很久，直到发现原因。  

[![本来打算用作50Hz滤波的，结果没用上。刚做好就发现了问题的真正所在。](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150122_004635.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150122_004635.jpg)  

> 本来打算用作50Hz滤波的，结果没用上。刚做好就发现了问题的真正所在。  

于是我放弃了运放这个想法，重新开始研究电路本身，发现当电阻为20K的时候，对声音的变化比较敏感，当声音很大时，波动能有1V，于是，我改用这个电路，经过一个耦合电容，整流桥，最后再进行一次滤波，然后发现就没有然后了，输出结果在声音不是很大时是一条直线，而声音比较大时，波形也有大概1.2V的衰减，这能忍？本来单片机的AD就不够强，这样一折腾，还搞啥。。。  而经过测试，在耦合电容处、整流桥前的波形都完全正常。于是，各种换电容，都没有满意的结果。  
突然，我意识到二极管是有正向压降的，这个特征也刚好符合衰减1.2V的情况。  
我最初想到的经济解决方法是在整流桥出增加1.2V的电压输入，转念一想，这样干扰了负半周的信号。黄大法提出在整流桥处分别加两个电压为+-1.5V的独立电源，不过，由于电源不容易在板子上实现，这个计划也泡汤了。我有开始在网上查找正向压降低的二极管，发现了一款0压降的，但是由于其只能工作在2V的电压下，所以也不能解决问题。其他的搜索结果只能说差强人意————使用这些二极管，我的信号损耗会从1.2V降到0.6V，这也不是一个很令人满意的数字。  
最后，我突然意识到一个问题：我之前之所以要将信号的交流部分分离出来，是因为当时我想将信号放大再处理，而我现在并没有放大信号的需要，所以我根本就不需要分离出交流信号，就更谈不上整流了。这样，二极管压降的问题就瞬间灰飞烟灭了。  
说做就做，我很快焊好了电路，进行了测试，效果不咋的。  
[![1](https://tec.hxlxz.com/wp-content/uploads/2015/01/12.png)](https://tec.hxlxz.com/wp-content/uploads/2015/01/12.png)  
我想，一不做二不休，大不了软件滤波！又把滤波电容去掉了。电路成了这样：

[![我是电路板，我是不是很简单？](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150122_004654.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150122_004654.jpg)  

> 我是电路板，我是不是很简单？  

效果出乎意料的好，一般声音的电压波动在1V左右，较大音量的在2-3V，对着话筒吹气，电压波动可达4.85V。电源电压是5V。  

[![瞬间波形的抓图](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150122_004351.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150122_004351.jpg)  

> 瞬间波形的抓图  

于是，就这样咯，到时候写程序多次取样取均值进行“软件滤波”，由于接受到的声音频率大都只有几百赫兹到几千赫兹，这款单片机的300KHz的AD完全够用了。  
所以，今天就到这里吧，软件啥的明天（其实还是今天）再说。  
来张我的4个失败品的合影：  

[![失败品合影](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150122_004619.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150122_004619.jpg)  

> 失败品合影  

好，就这样。

### **2015年2月4日（凌晨）**

这几天主要在搞器件的焊接和电路板的布线，所以，没有这么更新日志。  
今天，电路板的布线工作已经完成，并委托了PCB制板厂进行PCB打样生产。话说，做PCB板真TM贵，我的板子是19CM×27CM的，大部分厂家要价300-500大洋，最后找到一家良心PCB厂，140大洋搞定（5片），其实多的也没啥用，压箱底吧。加上运费和一本书，183大洋。顺便在次提醒一下，PCB板，如果能压缩到10CM×10CM以下，能省不少钱（这个规格的板子，基本所有厂家都有大幅优惠，大概50大洋10片）。  

[![20150205211911](https://tec.hxlxz.com/wp-content/uploads/2015/01/20150205211911.png)](https://tec.hxlxz.com/wp-content/uploads/2015/01/20150205211911.png)  

画PCB板子，布线也够烦的，陆陆续续搞了10来天才布好（包括原理图库和封装库的制作及器件硬件信息的查询和测量）  
PCB图将在项目完成后以[知识共享 署名-非商业性使用-相同方式共享 4.0 国际 许可协议（CC-BY-NC-SA 4.0)](http://creativecommons.org/licenses/by-nc-sa/4.0/) 开源。  

[![全板视图（没有显示覆铜）](https://tec.hxlxz.com/wp-content/uploads/2015/01/0.png)](https://tec.hxlxz.com/wp-content/uploads/2015/01/0.png)  

> 全板视图（没有显示覆铜） 

[![全板视图（顶层）](https://tec.hxlxz.com/wp-content/uploads/2015/01/13.png)](https://tec.hxlxz.com/wp-content/uploads/2015/01/13.png)  

> 全板视图（顶层）  

[![底层](https://tec.hxlxz.com/wp-content/uploads/2015/01/a3-12.png)](https://tec.hxlxz.com/wp-content/uploads/2015/01/a3-12.png)  

> 底层  

[![顶层](https://tec.hxlxz.com/wp-content/uploads/2015/01/a3-22.png)](https://tec.hxlxz.com/wp-content/uploads/2015/01/a3-22.png)  

> 顶层  

大概补下这几天的日志吧。  
23日，元件到手，进行了元件的测试。  

[![这次买的元件的全家福（LED已经被用掉一半）](https://tec.hxlxz.com/wp-content/uploads/2015/01/1423149600405.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/1423149600405.jpg)  

> 这次买的元件的全家福（LED已经被用掉一半） 

并通过调节限流电阻的阻值来使三色LED在5V电压下混合出白光。考虑到USB供电方式的电流限制，我把单个LED的电流限制在了10mA左右，这样，整个系统的工作电流不会超过1A，普通的充电宝和手机充电器都能为这个光立方供电。  

[![这个是第一次用的测试板，但由于选用的电位器阻值太大，不方便调节。](https://tec.hxlxz.com/wp-content/uploads/2015/01/1423144034617.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/1423144034617.jpg)  

> 这个是第一次用的测试板，但由于选用的电位器阻值太大，不方便调节。

[![这货是改进后的测试板，选用了更适合的电位器，添加了LED插座。](https://tec.hxlxz.com/wp-content/uploads/2015/01/142314424894381.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/142314424894381.jpg)  

> 这货是改进后的测试板，选用了更适合的电位器，添加了LED插座。  

测试得到的电阻值是：红780，绿850，蓝960。  
而这个阻值不是标准的阻值，于是，我采用了比较接近的阻值（红750，绿820，蓝910)。经过测试，效果还不错。  

[![1423147095769](https://tec.hxlxz.com/wp-content/uploads/2015/01/1423147095769.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/1423147095769.jpg)  

随后试制了一个二阶的全彩“光立方”，效果不错，但是在进行部分颜色显示时，部分LED有色差，后期需要检测、更换。  
[![IMG_20150123_004903](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150123_004903.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150123_004903.jpg)  

[![IMG_20150123_004947](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150123_004947.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150123_004947.jpg)  

[![IMG_20150123_005304](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150123_005304.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150123_005304.jpg)  
之后就是各种继续画图+焊接光立方的LED灯组。前面已经说到，PCB的设计已经完成并委托生产；LED灯组也完成了90%。鉴于本人的焊接技术略捉鸡（各种难看），LED的焊接是由一只一点也不萌的妹纸进行的。  

[![左边的是我做的，右边的是一点也不萌的妹纸做的。感觉被秒杀。。。](https://tec.hxlxz.com/wp-content/uploads/2015/01/1423148404923.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/1423148404923.jpg)  

> 左边的是我做的，右边的是一点也不萌的妹纸做的。感觉被秒杀。。。

我们自己设计了一种焊接支架，由一个电阻和一个DIP4器件（实验室可怜的运放啊）的引脚的一边组成，具体看来，是这样的。  

[![1423150010842](https://tec.hxlxz.com/wp-content/uploads/2015/01/1423150010842.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/1423150010842.jpg)  

使用起来，是这样的。  

[![不要问我为什么板子变黑了。。。其实是因为用热风枪除去板子上残余的松香，多几次就这样了](https://tec.hxlxz.com/wp-content/uploads/2015/01/1423148347659.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/1423148347659.jpg)  

> 不要问我为什么板子变黑了。。。其实是因为用热风枪除去板子上残余的松香，多几次就这样了  

后来，在焊接了3面灯板后，一点也不萌的妹纸发现这样单个焊接的灯间距精度不够，误差太大，于是，就有了这块板子。  

[![是不是高大上很多？](https://tec.hxlxz.com/wp-content/uploads/2015/01/1423148169316.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/1423148169316.jpg)  

> 是不是高大上很多？  

于是，LED部分就基本完成了，就待板子做好后进行测试再组装起来了。顺便提醒，要是不测试就把东西焊好，万一到时发现中间的一个灯挂了，哭都来不及。  

[![弯折好针脚等待焊接的灯](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150126_210245.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150126_210245.jpg)  

> 弯折好针脚等待焊接的灯  

[![一点也不萌的妹纸正在焊灯](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150125_214120.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150125_214120.jpg)  

> 一点也不萌的妹纸正在焊灯  

[![焊好的灯都在这里了](https://tec.hxlxz.com/wp-content/uploads/2015/01/1423147422469.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/1423147422469.jpg)  

> 焊好的灯都在这里了  

基本就这样了，现在开始写程序、做动画了。等板子回来再进行焊接工作。
（我猜那只一点也不萌的妹纸肯定不会看这篇文章，就算她看了也不会打死我的） 

### **2015年2月8日**

今天，定做的PCB板子到了，看上去还不错。  
[![PCB1](https://tec.hxlxz.com/wp-content/uploads/2015/01/PCB1.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/PCB1.jpg)  

[![PCB2](https://tec.hxlxz.com/wp-content/uploads/2015/01/PCB2.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/PCB2.jpg)  
然后就是焊东西上去、完成LED部分的最后焊接了。  
程序也开始写了，好麻烦的样子。幸好之前有一些积攒下来的模块可以直接用。  
也没啥好说的，就这样吧。  


### **2015年2月10日**


电路板算是焊好了，就是贴片元件焊起来好麻烦，还搞坏了几个。  
另外，不知道为什么，锁存器处于高阻态时，莫名其妙地产生了很大的电流（大概3A的样子），经过各种检查都没有找出原因。于是，作为补救，用一根导线将锁存器的OE引脚接到了GND上，解决了问题，不过，这始终治标不治本，这个问题，还得慢慢寻找答案。  
[![IMG_20150207_194942](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150207_194942.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150207_194942.jpg)  

[![IMG_20150207_194948](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150207_194948.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150207_194948.jpg)  
 
[![IMG_20150207_195005](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150207_195005.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150207_195005.jpg)  

[![IMG_20150208_185444](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150208_185444.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150208_185444.jpg)  

然后还重新检查了LED  
[![IMG_20150208_192504](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150208_192504.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150208_192504.jpg)  

[![IMG_20150208_193614](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150208_193614.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150208_193614.jpg)  

[![IMG_20150208_203901](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150208_203901.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150208_203901.jpg)  

[![IMG_20150208_203906](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150208_203906.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150208_203906.jpg)  

### **2015年2月11日-2015年3月23日**


这段时间基本没有做什么事，过年+准备高数补考。  
就是发现LED间距还是不对，需要调整。  
这是LED插上去的样子，可以看到LED还是不怎么整齐。  
[![IMG20150211222622](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG20150211222622.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG20150211222622.jpg)  

[![IMG20150211222907](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG20150211222907.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG20150211222907.jpg)  


### **2015年3月24日**


重新梳理了项目  
[![IMG_20150324_213934_HDR](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150324_213934_HDR.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150324_213934_HDR.jpg)  


### **2015年3月26日**


把LED全部插到了插座上，但通电后发现了一个严重的问题：在将led公共阳极悬空的情况下，部分led仍然微弱发光！  
在小睿睿的指导下，测得led两端存在高频振荡。  
[![IMG_20150326_175614_HDR](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150326_175614_HDR.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150326_175614_HDR.jpg)  
[![IMG_20150326_183244_HDR](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150326_183244_HDR.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150326_183244_HDR.jpg)  
[![IMG_20150326_175536_HDR](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150326_175536_HDR.jpg)](https://tec.hxlxz.com/wp-content/uploads/2015/01/IMG_20150326_175536_HDR.jpg)  
当时整个人都跟led一样高频振荡起来了，因为，如果高频振荡是导致led发光的原因，就意味着，我的整个电路板存问题，需要全部重做。  
[![XDWZD](https://tec.hxlxz.com/wp-content/uploads/2015/01/XDWZD-300x284.png)](https://tec.hxlxz.com/wp-content/uploads/2015/01/XDWZD.png)  
不过，我机智地重新检测了所有led，发现有三个灯被部分击穿，而且更幸运的是，这些灯都在光立方的最外层，更换后，问题解决。  
但是，解决了这个问题后，如果将led公共极接到vcc，一些led会被点亮，而且，这些被点亮的led还是随机的，在我想用单片机向所有锁存器发出指令以进行测试时，却怎么也写不进程序，原来是我的12挂了…  
更换后再次测试，问题未解决。  


### **2015年3月27日**


突然心血来潮，去搞了个github来玩，顺便把我已经写的代码上传到了[github](https://github.com/hxl9654/Multifun-Cube)上面，之前的所有开源模块我也都传到[这里](https://github.com/hxl9654/51freecode)了。具体，看[这篇文章](https://tec.hxlxz.com/p=337---2015-03-31)。  


### **2015年4月17日**

由于近期事情比较多，这个项目之后先暂停，等到稍微闲一点的时候再继续搞。  

《《《《未完待续》》》》   

[![知识共享许可协议](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-nc-sa/4.0/)  
不务正业的光立方项目日志（8阶全彩多功能光立方） 由 [何相龙]() 创作，采用 [知识共享 署名-非商业性使用-相同方式共享 4.0 国际 许可协议](http://creativecommons.org/licenses/by-nc-sa/4.0/)进行许可。  
[在Wordpress站上浏览本文](https://tec.hxlxz.com/?p=198)
