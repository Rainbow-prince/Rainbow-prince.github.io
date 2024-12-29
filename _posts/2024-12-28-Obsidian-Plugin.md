---
layout: post
title: Obsidian Plugin：为标题插入前缀
subtitle: “我的第一个obdisian插件”
author: Rainbow-Prince
header-mask: 0.2
header-img: img/bg-material.jpg
tags:
  - blog
  - Obsidian
---

> 程序员的三大美德：懒惰，急躁和傲慢

## 🌖缘起

这件事讲起来有点“大炮打蚊子”，为了懒惰而更加勤奋。

在昨天写个人博客的时候，我总觉得在阅读时，各个标题看起来观感不是很好，我希望能够是**每个标题都有一个emoji前缀，而且，各级emoji的前缀不同**。本着“懒惰是人类进步的阶梯”的原则，手动在标题前面添加emoji是不可能的😎

我是用Obsidian来编写个人博客的，目前我找不到市面上有存在这中插件，所以，我准备写一个Obsidian插件完成这个功能。

## 🌖流程

1. 识别标题
2. 如果标题未添加emoji前缀，则添加emoji前缀
3. 如果标题已经添加emoji前缀，则不管


## 🌖困难

- obsidian官方的api晦涩难懂——这几乎是所有obsidian插件新手开发者的阻碍
- 纯英文的开发文档让我头昏眼花
- 我完全不知道要从哪里入手


## 🌖解决

我找到一个“模板”，比一般我们用到的[obsidian-sample-plugin](https://github.com/obsidianmd/obsidian-sample-plugin)这个模板要更简单一点，配合obsidian的另一个插件叫[hot-reload](https://github.com/pjeby/hot-reload)，就可以直接在obsidian中开发js啦

可以参考下面的文章
- [史上最简单易用的obsidian插件开发方法（适合新手） - 开发讨论 - Obsidian 中文论坛](https://forum-zh.obsidian.md/t/topic/37149)
- [模板下载](https://github.com/wish5115/my-softs/releases/download/ObsidianSample/obsidian-sample.zip)

此外，借助了kimi以及Marscode，经历一天时间，终于初步完成了这个插件。

## 🌖结语 & 日志

%% - 🚩**2024年12月29日**： %%
- 🚩**2024年12月28日**：完成基本的 添加/移除 前缀 功能
- 🚩**2024年12月27日**：着手开发

