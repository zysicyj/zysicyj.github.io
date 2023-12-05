---
uuid: b6560190-4982-11ee-a839-553a00b959d8
title: 给Hexo添加说说功能
tags:
  - Hexo
  - 说说功能
  - 文章
  - 插件
  - 技术
  - 教程
abbrlink: 82b271f
date: 2023-09-02 19:20:24
---


> 有的时候博客内容会有变动，首发博客是最新的，其他博客地址可能会未同步,认准`https://blog.zysicyj.top`

> 全网最细面试题手册，支持艾宾浩斯记忆法。这是一份最全面、最详细、最高质量的 java
面试题，不建议你死记硬背，只要每天复习一遍，有个大概印象就行了。 `https://store.amazingmemo.com/chapterDetail/1685324709017001`
    

[官网地址](https://artitalk.js.org/doc.html)


---

# 效果

![](http://blog-1253652709.cos.ap-guangzhou.myqcloud.com/pasteimageintomarkdown/2023-09-02/78606840375800.png)

# 👀 前言

-----

GitHub 仓库：[Artitalk.js](https://github.com/ArtitalkJS/Artitalk)

## 🎉 特性

* 增删查改全方面支持
* 支持针对每条说说的评论
* 支持 Markdown/html 语法
* 支持图片上传

# 🚀 快速使用

---

下列主题已将本项目整合进去，可以直接使用。 感谢以下主题对本项目的支持~

## [hexo-theme-volantis](https://github.com/xaoxuu/hexo-theme-volantis/)

## [hexo-theme-cards](https://github.com/ChrAlpha/hexo-theme-cards)

## [hexo-theme-butterfly](https://github.com/jerryc127/hexo-theme-butterfly)

## [hexo-theme-matery](https://github.com/blinkfox/hexo-theme-matery/)

## [gridea-theme-dark](https://github.com/jalenchuh/gridea-theme-dark)

## [hexo-theme-MengD](https://github.com/lete114/hexo-theme-mengd/)

# 🚀 开始使用

---

## 🌈 LeanCloud 的相关准备

TIP

**🎃 与 Valine 在同一个页面使用**

如果迫切需要将 Artitalk 与 Valine 在同一个页面使用，可以通过 Artitalk 与 Valine 使用同一个 LeanCloud 的应用来解决。

**🌍 建议使用国际版的 LeanCloud**

因为国际版的 LeanCloud 不需要配置 serverurl，所以推荐使用国际版，速度没有区别，如果使用国内版的 LeanCloud 别忘了填写
serverurl 即可

👀 与valine在同一页面使用

如果有这个需要，可以将 artitalk 与 valine 存放在同一个应用中。可以有效避免同一个页面使用两个leancloud应用所产生的冲突。

1. 前往 [LeanCloud 国际版](https://leancloud.app/)，注册账号。
2. 注册完成之后根据 LeanCloud 的提示绑定手机号和邮箱。
3. 绑定完成之后点击`创建应用`，应用名称随意，接着在`结构化数据`中创建 `class`，命名为 `shuoshuo`。
4. 在你新建的应用中找到`结构化数据`下的`用户`。点击`添加用户`，输入想用的用户名及密码。
5. 回到`结构化数据`中，点击 `class` 下的 `shuoshuo`。找到权限，在 `Class 访问权限`中将 `add_fields` 以及 `create`
   权限设置为指定用户，输入你刚才输入的用户名会自动匹配。为了安全起见，将 `delete` 和 `update` 也设置为跟它们一样的权限。
6. 然后新建一个名为`atComment`的class，权限什么的使用默认的即可。
7. 点击 `class` 下的 `_User` 添加列，列名称为 `img`
   ，默认值填上你这个账号想要用的发布说说的头像url，这一项不进行配置，说说头像会显示为默认头像 —— Artitalk 的 logo。
8. 在最菜单栏中找到设置-\> 应用 keys，记下来 `AppID` 和 `AppKey` ，一会会用。
9. 最后将 `_User` 中的权限全部调为指定用户，或者数据创建者，为了保证不被篡改用户数据以达到强制发布说说。

❗ 关于设置权限的这几步

这几步一定要设置好，才可以保证不被 “闲人” 破解发布说说的验证

## 🌼 开始使用

## 🎅 配置项的说明

可以通过修改配置项快捷更改部分功能，[点我查看详细说明](https://artitalk.js.org/settings.html)

## 🔨 测试使用

如果上面的配置没有问题，打开你的页面，点击页面右下角的登录输入用户密码后，在输入框中输入说说，点击发布即可。

## 🔨 说说内容的删除

登录后点击说说内容框右上角的 x，点击确定删除即可。

## 🔨 说说内容的修改

点击想要修改的那条说说的头像，会自动跳转到只有一条提示语以及输入框的界面，在输入框中编辑完之后点击保存即可

注：说说内容的修改与删除在 LeanCloud 后台也可进行操作

## 🔨 评论的使用

点击每条说说右下角的评论图标即可查看针对本条说说的评论或者对本条说说发起评论，再次点击会刷新页面已达到返回的作用

填写邮箱以获得 gravatar 的头像

## 🦄 在 Typecho 中使用

---
---

1. 登陆后台后新增独立页面
2. 标题随意填，内容填为

3. 发布页面

## 🍖 在 Vue 单页项目中使用

---
---

例如 vuepress Gridsome 等博客框架是由 Vue 构建的。

在Gridsome中的准备

在`gridsome.config.js`中引入 artitalk

在普通Vue项目中的准备

在`<YOUR_PROJ>/public/index.html`中引入 artitalk

新建 `src/components/Artitalk.vue`（VuePress: `.vuepress/components/Artitalk.vue`），添加以下内容

如果需要加入 Artitalk 的页面为 `.md`（例如 VuePress），直接在其中写入 `<Artitalk />` 即可。

如果为 `.vue` （开发项目） 除了写入 `<Artitalk />`，还需要加入以下内容

## 🚀 安全性

----

由于 leancloud 的机制，应用的 Appid 以及 Appkey 均会暴漏在前端，可能会遭受到其他人的恶意攻击。
如果你在担心这个问题，你可以使用[Artitalk_SafeMode](https://artitalk.js.org/settings.html/Artitalk_SafeMode)

## 🕸 使用 cdn

----

### 🕸 UNPKG

#### ⭐ 获取最新

#### 🍳 获取指定版本

使用指定版本，在版本号填上对应版本即可，例如：[https://unpkg.com/artitalk@1.1.15/artitalk.js](https://unpkg.com/artitalk@1.1.15/artitalk.js)

关于版本可查看：[https://unpkg.com/artitalk/](https://unpkg.com/artitalk/)

### 🕸 JsDelivr（国内无法使用！！！）

#### ⭐ 获取最新

#### 🍳 获取指定版本

使用指定版本，在版本号填上对应版本即可，例如：[https://cdn.jsdelivr.net/npm/artitalk@1.1.15](https://cdn.jsdelivr.net/npm/artitalk@1.1.15)

关于版本可查看：[https://cdn.jsdelivr.net/npm/artitalk/](https://cdn.jsdelivr.net/npm/artitalk/)


