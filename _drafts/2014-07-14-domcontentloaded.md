---
layout: post
title: "DOMReady相关"
description: ""
category: notes
tags: []
---
{% include JB/setup %}

document的readyState属性：当前document加载状态，有这几种表示加载完成（loaded|in|complete）。

document的DOMContentLoaded事件：当DOM内容加载完成并且经过处理后触发，不论样式，图片是否加载完成。用于动态加载元素（或JS）时，等载入完成后再做一些事情。

具体用法参考[domready][lnk-domready]

[lnk-domready]:https://github.com/ded/domready/blob/master/src/ready.js
