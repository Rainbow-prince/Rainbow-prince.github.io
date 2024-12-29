---
layout: post
title: 【合集】blog 问题 & 方法
subtitle: “九九八十一难”
author: Rainbow-Prince
mathjax: true
header-mask: 0.2
header-img: img/alex-dukhanov-ZxZQk7777R4-unsplash.jpg
tags:
  - blog
---
小白，在写博客的过程中遇到很多困难，在此做记录，愿为后来者指路。**此文将长期更新，文章结构将不断调整。**




### 🌗通过github page部署太慢，无法实时预览

根据Hux（就是这个博客模板的原作者）的教程，是可以在本地预览的，但是需要部署好`jekyll`环境。如果什么环境都没有，那么请参考官方的部署文档，写的很详细——[Jekyll on Windows \| Jekyll • Simple, blog-aware, static sites](https://jekyllrb.com/docs/installation/windows/)


可能会遇到执行某些命令行（比如`ridk install`）的时候 **“无响应”或者“卡住”等情况** ，大概率网络有问题，**换网络、加代理、或者换源**可以解决。*对于我自己，换源又有新报错了，最后是用原来的源，等待一段时间之后突然可以下载了*

部署好之后，在本地运行`jekyll serve` 或者 `jekyll serve --watch`，可在本地浏览器**实时预览**，浏览器刷新即可更新


### 🌗实时预览卡顿

在本地运行`jekyll serve` 或者 `jekyll serve --watch`实时预览的时候，进行文本编辑出现卡顿，目前我的解决方法是：**写完再预览🥲，总比到github上看要快得多的**


### 🌗用什么编辑器写blog

我用的是obsidian，好处是：
- 实时预览markdown渲染后的效果
- 图片路径发生更改时（比如你改名字、移动到别的文件夹等），会在引用处（比如你的文章那里）自动更新路径
- ctrl+左键点击图片可跳转到该图片，还可以显示其路径

### 🌗实时预览无法显示图片
原因众多，我收集了我自己遇到的问题，作为参考如下：

#### 🌘【obsidian】图片的 路径 or 格式 有问题

本人用的是 `obsidian` 笔记软件作为我的文章的编辑器，其默认的图片路径为`！[[路径]]`

![](/img/Pasted%20image%2020241227112918.png)

关闭此选项，就可以使用标准的markdown语法的链接格式 `![]()` 。可能你会发现在实时预览的时候**还是显示不了图片**。这个时候可能是**路径问题**。

![](/img/Pasted%20image%2020241227114707.png)

比如我上面这种照片的路径为 `![](/img/Pasted%20image\%2020241227112918.png)`，但其实应该改为`![](/img/Pasted%20image%2020241227112918.png)`，也就是在路径的最前面加一个斜杠 `/`。因为无法直接在obsidian设置修改成这种格式，需要借助obsidian的插件[Regex Find and Replace](https://pkmer.cn/Pkmer-Docs/10-obsidian/obsidian%E7%A4%BE%E5%8C%BA%E6%8F%92%E4%BB%B6/readme/obsidian-regex-replace_readme/)（插件安装教程在网上有不少），根据正则表达式查找并更改。

![](/img/Pasted%20image%2020241227113739.png)


**仅供参考：**
```
find: !\[\]\(img/(.+?)\)
replace: ![](/img/$1)
```

一键替换之后，原本只能在Obsidian里面预览的照片，现在能在浏览器预览啦~


### 如何在个人博客渲染Latex代码

Hux的博客模板中，已经包含了相关的文件，
![](img/Pasted%20image%2020241229140955.png)

只需要在配置文章开头的yaml配置中设置，即可渲染latex代码，如下
```yml
mathjax: true
```


```
$inline~math$
```
$inline~math$

```
$
  \begin{align}
    mathblock
  \end{align}
$

\begin{align}
	mathblock
\end{align}

```
$
  \begin{align}
    mathblock
  \end{align}
$

  \begin{align}
    mathblock
  \end{align}