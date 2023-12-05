---
uuid: 78face60-47cb-11ee-a762-4323edd864dc
title: 【Linux系列】离线安装openjdk17的rpm包
tags:
  - Linux
  - RPM
  - Java
categories:
  - 技术文章
  - 后端技术
  - 系列文章
abbrlink: 6a27ead0
date: 2023-08-31 14:56:12
---


> 有的时候博客内容会有变动，首发博客是最新的，其他博客地址可能会未同步,认准`https://blog.zysicyj.top`



> 全网最细面试题手册，支持艾宾浩斯记忆法。这是一份最全面、最详细、最高质量的 java
面试题，不建议你死记硬背，只要每天复习一遍，有个大概印象就行了。 `https://store.amazingmemo.com/chapterDetail/1685324709017001`
    

[系列文章地址](https://blog.zysicyj.top/categories/技术文章/后端技术/系列文章/Linux/)

<div class="bilibili">
   <iframe src="//player.bilibili.com/player.html?bvid=BV1Lu4y1Q73x&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>
</div>

## 准备RPM包

请从官网下载：[https://www.oracle.com/java/technologies/downloads/#java17](https://www.oracle.com/java/technologies/downloads/#java17)

如需不限速下载，请关注【程序员朱永胜】并回复1020获取。

![](http://blog-1253652709.cos.ap-guangzhou.myqcloud.com/pasteimageintomarkdown/2023-08-31/96087357359900.png)

## 安装

``` shell
yum localinstall jdk-17_linux-x64_bin.rpm
```

![](http://blog-1253652709.cos.ap-guangzhou.myqcloud.com/pasteimageintomarkdown/2023-08-31/99225422297200.png)

## 验证

``` shell
java -version
```

![](http://blog-1253652709.cos.ap-guangzhou.myqcloud.com/pasteimageintomarkdown/2023-08-31/99250449167000.png)


