---
layout: post
title: What's iframe?
subtitle: “more cool blog”
author: Rainbow-Prince
header-mask: 0.5
header-img: img/bg-post-wall.jpg
tags:
  - blog
  - html
---

为了做出更好看的博客，为了能在文章里面加入幻灯片， iframe是不得不学的。

## 🌖IFRAM 是什么?

IFRAM是一个HTML的标签，是个内联框架。它其实很像Obsidian的一个插件——Excalidraw中的一个工具：在画板的里面嵌入一个页面，并且可以实现和那个页面的实时交互。就相当于在你自己的页面内开了一个小窗口：

![](/img/iframe-excalidraw-demo.png)

如果你想在页面中插入iframe，可以使用如下代码：

```html
<iframe src="想要展示的页面的网址" frameborder="0"></iframe>
```

比如说，这个是黄玄的一个幻灯片的页面。使用iframe将它嵌套到我的页面里，效果如下：
<br>
<br>
<br>
<style>
    .iframe-container {
        display: grid;
        place-items: center; /* 水平和垂直居中 */
		transform: scale(2); /* 放大 */
    }
</style>
<div class="iframe-container">
    <iframe src="http://huangxuan.me/js-module-7day/" frameborder="0"></iframe>
</div>
<br>
<br>
<br>
如果你用的是 Obsidian 作为编辑器的话，你可以直接在你的编辑器里面看到这个元素的源码和渲染后的效果：

![](/img/iframe-demo.png)
``

## 🌖优点 & 缺点

### 🌗优点
1. 有目共睹的简单

2. 对于通用的页面，通过iframe嵌套，可以**提高代码的重用率**。比如页面的头部样式和底部版权信息

3. 重新加载页面时，不需要重载iframe框架页的内容，**增加页面重载速度**


### 🌗缺点

1. 如果在一个页面中，加载了多个 iframe，可能会导致网页的性能下降，其实就相当于你同时要打开很多个网页

2. 正因为iframe与当前的页面相隔离，很可能你浏览器的插件就无法识别到iframe上的元素。比如网页翻译软件


## 🌖参考文章
- [什么是iframe及作用是什么？ - 石海莹 - 博客园](https://www.cnblogs.com/shihaiying/p/11415605.html)
- [什么是iframe？请讲述一下iframe的优缺点？-阿里云开发者社区](https://developer.aliyun.com/article/1366435)
