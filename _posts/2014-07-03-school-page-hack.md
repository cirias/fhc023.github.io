---
layout: post
title:  '学生信息管理系统－黑科技'
date:   2014-07-03 20:59:07
categories: hack
---

{% include JB/setup %}

------

## 更新

* 2014-07-09 修复“我的奖学金”始终在载入
* 2014-07-18 修复“资助管理”下三个链接始终在载入
* 2014-07-21 新增“绩点查看”支持

------

## 简介

为了解决学校网站只有特定IE浏览器才能登录的问题，自主开发的**黑科技**。

[学生信息管理系统][lnk-school-page]这个网站上的一些按钮，在Chrome，Safari，Firefox，Opera等主流浏览器上点了没反应。
必须要用特殊的IE版本才能正常操作，这很不方便，有木有。

于是，借助黑科技的力量，我将它在所有浏览器上都能正常操作，不再会有没反应的情况发生。

不再为找不到合适浏览器担忧！

不再为切换浏览器而烦恼！

~~*PS:*目前仅支持[学生信息管理系统][lnk-school-page]。~~

------

## 使用

1. <a class="btn" id="page_hack_js">请把我拖到书签栏</a> *或者* 复制下面所有代码，并保存成书签。

2. 进入**并登录**[学生信息管理系统][lnk-school-page]。

3. 点击刚才新建的书签，于是奇迹自然就发生了……

```javascript
javascript:!function(a,b,c){function d(){a.hacking=!0,h.id="mask",h.style.position="absolute",h.style.zIndex="1",h.style.width=b.body.scrollWidth+"px",h.style.height=b.body.scrollHeight+"px",h.style.top="0px",h.style.left="0px",h.style.background="#000",h.style.filter="alpha(opacity=40)",h.style.opacity="0.40",g.appendChild(h),b.lastChild.appendChild(g)}function e(){b.lastChild.removeChild(g),a.hacking=!1}function f(){a.hacked?e():setTimeout(f,50)}if(!a.hacked&&!a.hacking){var g=b.createElement("body"),h=b.createElement("div"),i=b.createElement("script");i.setAttribute("src","http://fhc023.github.io/stuff/school-page-hack/"+c.host.split(":")[0]+".min.js"),i.setAttribute("charset","utf-8"),b.getElementsByTagName("head")[0].appendChild(i),d(),f()}}(window,document,location);
```

<script type="text/javascript" src="/javascript/load_page_hack.js"></script>

------

## 备注
* 由于生活日益繁忙，不能保证更新速度，在这里贴上[源码地址][lnk-source-url]，注释会抽空补上。如果有紧急问题，大家可以自己fork。
* 2014-07-21之后的更新（不包括2014-07-21），不用再重新创建书签，直接使用原有的书签即可。

[lnk-school-page]:http://sam.sit.edu.cn
[lnk-source-url]:https://github.com/fhc023/school-page-hack
