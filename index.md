---
layout: page
title: 蜀相记
tagline: Chase the Excellence, Success will follow you.  
---
{% include JB/setup %}

你好，欢迎来到我在GitHub上的博客。  
我是一只热爱编程的程序猿，不过现在仍然学艺不精，距离大牛还很远。  
本博客还有[wordpress版](https://tec.hxlxz.com)，留言、互动可以去那里。  

## 我的博文 ##
<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>