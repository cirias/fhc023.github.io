---
layout: post
title:  "学生信息管理系统－多浏览器支持（黑科技）"
date:   2014-07-03 20:59:07
categories: hack
---

## 简介

大家都知道，学校网站实在是坑得不行，尤其是只能用特殊版本的IE才能访问的某些页面。
实在是太闹心了。

为了避免这种操蛋的事情影响我脆弱的神经系统，必须得将其铲除！！

为此，我不得不出卖灵魂，祭出**黑科技**法宝！

*PS:*目前仅支持[学生信息管理系统][lnk-school-page]。

## 使用

+ 选中下面整行代码，拖至浏览器书签栏。

```
javascript:(function(e,f,g){if(g.hacking){return}g.hacking=true;var h=e.createElement("body");var j=e.createElement("div");j.id='mask';j.style.position="absolute";j.style.zIndex="1";j.style.width=e.body.scrollWidth+"px";j.style.height=e.body.scrollHeight+"px";j.style.top="0px";j.style.left="0px";j.style.background="#000";j.style.filter="alpha(opacity=40)";j.style.opacity="0.40";h.appendChild(j);e.lastChild.appendChild(h);var k=f.getElementsByTagName("HEAD")[0];var l=f.createElement("SCRIPT");l.setAttribute("type","text/javascript");l.setAttribute("src","http://fhc023.github.io/javascript/prototype.js");k.appendChild(l);setTimeout(function(){var a=f.createElement("SCRIPT");a.setAttribute("type","text/javascript");a.setAttribute("src","http://code.jquery.com/jquery-1.3.2.min.js");k.appendChild(a)},1000);setTimeout(function(){var a=f.createElement("SCRIPT");a.setAttribute("type","text/javascript");var b=f.createTextNode("var jqy = jQuery.noConflict();");a.appendChild(b);k.appendChild(a)},1500);setTimeout(function(){g.$=function(a){if(arguments.length>1){for(var i=0,elements=[],length=arguments.length;i<length;i++)elements.push($(arguments[i]));return elements}if(typeof a=='string')a=f.getElementById(a);return g.Element.extend(a)}},1500);g.setUrl=function(b,c){g.jqy("#urlName").val(b);g.jqy("#urlAdress").val(c);var d=g.jqy("#setURLName").serialize();g.jqy.ajax({type:"POST",url:"/loadFunctionNamePage.jsp",data:d,success:function(a){}})};setTimeout(function(){e.lastChild.removeChild(h);g.hacking=false},2000)})(document,document.getElementsByName("contents")[0].contentDocument.getElementsByName("dtbar")[0].contentDocument,document.getElementsByName("contents")[0].contentDocument.getElementsByName("dtbar")[0].contentWindow);
```

+ 进入并登录[学生信息管理系统][lnk-school-page]。

+ 点击刚才新建的书签，此时页面会变暗，待页面恢复后即可操作。



[lnk-school-page]:http://sam.sit.edu.cn
