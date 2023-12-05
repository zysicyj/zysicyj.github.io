---
uuid: a74dff2b-4416-11ee-9ac2-67d3233bf96f
title: 配置Picgo图床之COS、OSS、Github图床
tags:
  - PicGo
  - 图床
  - Github
  - COS
  - OSS
  - 图片上传
  - 图片压缩
  - 图片编辑
  - 图片管理
  - 自定义配置
abbrlink: e27b9279
date: 2023-08-07 19:50:31
---


## 简介

PicGo是一款开源的图片上传和管理工具，它提供了简单易用的界面和丰富的功能，方便用户上传、管理和分享图片。

以下是PicGo的一些主要特点和功能：

1. 图片上传：PicGo支持将本地图片快速上传到云存储服务，如七牛云、腾讯云、阿里云等。你可以选择自己喜欢的云存储服务，并通过PicGo将图片批量上传到云端。

2. 图片压缩：PicGo内置了图片压缩功能，可以帮助你在上传图片之前对图片进行压缩，减小图片文件大小，提高网页加载速度。

3. 图片编辑：PicGo提供了简单的图片编辑功能，包括裁剪、旋转、调整亮度、对比度等。你可以在上传图片之前对图片进行一些基本的编辑操作。

4. 图片管理：PicGo可以帮助你管理上传的图片，包括查看上传记录、复制图片链接、删除图片等。你可以方便地管理自己上传的图片，并在需要时获取图片链接进行分享。

5. 自定义配置：PicGo支持自定义配置，你可以根据自己的需求设置上传的命名规则、存储路径、图片样式等。这样可以更好地满足个性化的需求。

总的来说，PicGo是一款功能强大且易于使用的图片上传和管理工具，适用于个人用户、开发者和博主等多种场景。它可以帮助你更高效地上传、管理和分享图片。

## 准备PicGo

官网下载地址：https://github.com/Molunerfinn/picgo/releases

关注【程序员朱永胜】回复【1012】获取安装包，免费高速下载

## 配置Github

### 获取Token

![image-20230807200430847](https://blog-1253652709.cos.ap-guangzhou.myqcloud.com/blog/202308072004107.png)

![](https://blog-1253652709.cos.ap-guangzhou.myqcloud.com/blog/202308072005596.png)

![](https://blog-1253652709.cos.ap-guangzhou.myqcloud.com/blog/202308072005838.png)

### 创建仓库

随便创建一个仓库即可，我创建的是`pic`仓库

![image-20230807200705649](https://blog-1253652709.cos.ap-guangzhou.myqcloud.com/blog/202308072007898.png)

### 配置PicGo

![](https://blog-1253652709.cos.ap-guangzhou.myqcloud.com/blog/202308072007590.png)

## 配置腾讯云COS

### 获取Token

![image-20230807200848497](https://blog-1253652709.cos.ap-guangzhou.myqcloud.com/blog/202308072008733.png)

![image-20230807200924438](https://blog-1253652709.cos.ap-guangzhou.myqcloud.com/blog/202308072009686.png)

### 创建存储桶

![](https://blog-1253652709.cos.ap-guangzhou.myqcloud.com/blog/202308072010800.png)

设置为公有读私有写

![image-20230807201130106](https://blog-1253652709.cos.ap-guangzhou.myqcloud.com/blog/202308072011353.png)

参考下面模版填写

![image-20230807201157858](https://blog-1253652709.cos.ap-guangzhou.myqcloud.com/blog/202308072011921.png)

## 设置阿里云OSS

### 获取密钥

![image-20230807201312297](https://blog-1253652709.cos.ap-guangzhou.myqcloud.com/blog/202308072013528.png)

![image-20230807201333924](https://blog-1253652709.cos.ap-guangzhou.myqcloud.com/blog/202308072013156.png)

### 创建Bucket

![image-20230807201403715](https://blog-1253652709.cos.ap-guangzhou.myqcloud.com/blog/202308072014937.png)

### 参考下面模版

![image-20230807201422903](https://blog-1253652709.cos.ap-guangzhou.myqcloud.com/blog/202308072014966.png)

![image-20230807201500562](https://blog-1253652709.cos.ap-guangzhou.myqcloud.com/blog/202308072015802.png)
qcloud.com/blog/202308072015802.png)


