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

------

## 简介

大家都知道，学校网站实在是坑得不行，尤其是只能用特殊版本的IE才能访问的某些页面。
实在是太闹心了。

为了避免这种操蛋的事情影响我脆弱的神经系统，必须得将其铲除！！

为此，我不得不出卖灵魂，祭出**黑科技**法宝！

额，废话说多了……

[学生信息管理系统][lnk-school-page]这个网站上的一些按钮，在Chrome，Safari，Firefox，Opera等主流浏览器上点了没反应。
必须要用特殊的IE版本才能正常操作，这很不方便，有木有。

于是，借助黑科技的力量，我将它在所有浏览器上都能正常操作，不再会有没反应的情况发生。

不再为找不到合适浏览器担忧！！

不再为切换浏览器而烦恼！！！

*PS:*目前仅支持[学生信息管理系统][lnk-school-page]。

------

## 使用

1. <a class="btn" id="page_hack_js">请把我拖到书签栏</a> *或者* 复制下面所有代码，并保存成书签。

2. 进入**并登录**[学生信息管理系统][lnk-school-page]。

3. 点击刚才新建的书签，于是奇迹自然就发生了……

```javascript
javascript:!function(a,b,c){function d(){l.id="mask",l.style.position="absolute",l.style.zIndex="1",l.style.width=a.body.scrollWidth+"px",l.style.height=a.body.scrollHeight+"px",l.style.top="0px",l.style.left="0px",l.style.background="#000",l.style.filter="alpha(opacity=40)",l.style.opacity="0.40",k.appendChild(l),a.lastChild.appendChild(k)}function e(){a.lastChild.removeChild(k)}function f(a){c.alert(a)}function g(a,c){var d=b.createElement("SCRIPT");d.setAttribute("type","text/javascript"),d.setAttribute("src",j[c]),a.appendChild(d)}function h(a,b,d){var e=50;setTimeout(function(){c[a]?d():0>b?d("Error: timeout."):h(a,b-e,d)},e)}function i(a,b,c,d){g(a,b),h(b+"_loaded",c,d)}if(!c.hacking){c.hacking=!0;var j={prototype:"http://fhc023.github.io/stuff/school-page-hack/prototype.js",jquery:"http://fhc023.github.io/stuff/school-page-hack/jquery-1.3.2.min.js"},k=a.createElement("body"),l=a.createElement("div"),m=b.getElementsByTagName("HEAD")[0];d(),i(m,"prototype",5e3,function(d){d?(f(d),location.reload()):i(m,"jquery",5e3,function(d){function g(){var b=a.getElementsByName("main")[0].contentDocument,c=a.getElementsByName("main")[0].contentWindow;if(3===b.getElementsByTagName("body").length){var d=b.getElementsByTagName("body")[1].parentNode,e=b.getElementsByTagName("body")[1],f=b.getElementsByTagName("body")[2];d.removeChild(e),d.removeChild(f),c.ms_loadUrl=function(a){new c.Ajax.Request(a,{method:"post",onComplete:function(a){c.$("ms_view").innerHTML=a.responseText}})}}else setTimeout(g,50)}if(d)f(d),location.reload();else{var h=c.jQuery.noConflict();c.$=function(a){if(arguments.length>1){for(var d=0,e=[],f=arguments.length;f>d;d++)e.push($(arguments[d]));return e}return"string"==typeof a&&(a=b.getElementById(a)),c.Element.extend(a)},c.setUrl=function(a,b){h("#urlName").val(a),h("#urlAdress").val(b);var c=h("#setURLName").serialize();h.ajax({type:"POST",url:"/loadFunctionNamePage.jsp",data:c,success:function(){}})}}c.loadPage=function(a){switch(a){case 1:c.loadMask("/jxjgl/studentjxj!myScholarship.action","\u60a8\u5f53\u524d\u7684\u4f4d\u7f6e\uff1a\u8bc4\u4f18\u7ba1\u7406>>","\u5956\u5b66\u91d1\u7ba1\u7406","\u6211\u7684\u5956\u5b66\u91d1");break;case 2:c.loadMask("/zxjgl/studentzxj!myScholarship.action","\u60a8\u5f53\u524d\u7684\u4f4d\u7f6e\uff1a\u8d44\u52a9\u7ba1\u7406>>","\u52a9\u5b66\u91d1\u7ba1\u7406","\u6211\u7684\u52a9\u5b66\u91d1");break;case 3:c.loadMask("/knsgl/studentkns!myScholarship.action","\u60a8\u5f53\u524d\u7684\u4f4d\u7f6e\uff1a\u8d44\u52a9\u7ba1\u7406>>","\u56f0\u96be\u751f\u7ba1\u7406","\u6211\u7684\u56f0\u96be\u751f");break;case 4:c.loadMask("/jttfsjgl/studentjttfsj!myScholarship.action","\u60a8\u5f53\u524d\u7684\u4f4d\u7f6e\uff1a\u8d44\u52a9\u7ba1\u7406>>","\u56f0\u96be\u751f\u7ba1\u7406","\u6211\u7684\u5bb6\u5ead\u7a81\u53d1\u4e8b\u4ef6")}g()},b.getElementById("4af8a07a23e0a0820123e0ab2b61000d").childNodes[1].childNodes[1].setAttribute("onclick","loadPage(1);"),b.getElementById("4af8a07923e0e5430123e0fd2bc00026").childNodes[1].childNodes[1].setAttribute("onclick","loadPage(2);"),b.getElementById("4af8a07425d9a5980125d9ac4bb30004").childNodes[1].childNodes[1].setAttribute("onclick","loadPage(3);"),b.getElementById("4af8a07425d9a5980125d9ac4bb30004").childNodes[3].childNodes[1].setAttribute("onclick","loadPage(4);"),f("Hack success! "),e()})})}}(document,document.getElementsByName("contents")[0].contentDocument.getElementsByName("dtbar")[0].contentDocument,document.getElementsByName("contents")[0].contentDocument.getElementsByName("dtbar")[0].contentWindow);
```

<script type="text/javascript" src="/javascript/load_page_hack.js"></script>


[lnk-school-page]:http://sam.sit.edu.cn
