---
uuid: 6c475180-4aea-11ee-a68c-65f91bdbbcdb
title: 工作五年多，idea插件推荐（未完）
tags:
  - idea插件
  - Easy Javadoc
  - Transaction
  - .ignore
  - Atom Material Icons
  - Batch Scripts support
  - Camel Case
  - Chinese Language Pack
  - code glance pro
  - Dto Generator
  - EasyCode MybatisCodeHelper
  - GenerateAllSetter
categories: []
abbrlink: 4650d5de
date: 2023-09-24 08:15:19
---


> 有的时候博客内容会有变动，首发博客是最新的，其他博客地址可能会未同步,认准`https://blog.zysicyj.top`

> 全网最细面试题手册，支持艾宾浩斯记忆法。这是一份最全面、最详细、最高质量的 java
面试题，不建议你死记硬背，只要每天复习一遍，有个大概印象就行了。 `https://store.amazingmemo.com/chapterDetail/1685324709017001`
    



---

本来打算一次更新完的。。感觉还是太多了，后面再分享吧，先分享一部分

# EasyCode MybatisCodeHelper

这玩意功能太离谱了，随便举几个

官网地址：https://brucege.com/pay/view?code=dxAMx71

![数据库生成CRUD](http://blog-1253652709.cos.ap-guangzhou.myqcloud.com/pasteimageintomarkdown/2023-09-24/59355969033300.png)

![功能清单](http://blog-1253652709.cos.ap-guangzhou.myqcloud.com/pasteimageintomarkdown/2023-09-24/59191925967100.png)

![方法名生成sql](http://blog-1253652709.cos.ap-guangzhou.myqcloud.com/pasteimageintomarkdown/2023-09-24/59210338861400.png)

![生成mybatisplus query wrapper](http://blog-1253652709.cos.ap-guangzhou.myqcloud.com/pasteimageintomarkdown/2023-09-24/59257523947000.png)

![自动补全](http://blog-1253652709.cos.ap-guangzhou.myqcloud.com/pasteimageintomarkdown/2023-09-24/59282602326400.png)

![OGNL支持](http://blog-1253652709.cos.ap-guangzhou.myqcloud.com/pasteimageintomarkdown/2023-09-24/59297174924000.png)

![生成建表语句](http://blog-1253652709.cos.ap-guangzhou.myqcloud.com/pasteimageintomarkdown/2023-09-24/59329484236300.png)

# Easy Javadoc

Easy Javadoc是一个IntelliJ IDEA的插件，它能够帮助Java和Kotlin开发者自动生成Javadoc和Kdoc文档注释。该插件支持多种翻译服务，可以根据方法名自动翻译注释内容，并支持自定义映射。同时，Easy
Javadoc还支持选中中文进行翻译，无需切换到其他工具。

安装Easy Javadoc插件非常简单，只需要在IntelliJ IDEA的插件页面搜索"Easy Javadoc"，然后点击安装并重启IDEA即可。

使用Easy Javadoc插件也非常方便。你可以将光标放置在想要生成注释的类、方法或属性上，然后按下快捷键"ctrl \"（Windows）或"command
\"（Mac）即可生成注释。插件会根据方法名自动生成注释，你只需要补充具体的描述即可。此外，你还可以选中中文进行翻译，或者自定义映射来提高翻译的准确性。

Easy Javadoc插件还支持批量生成文档注释和自定义模板，方便快捷地生成多个类的注释。你可以在插件的配置页面进行相关设置，包括选择翻译服务、自定义映射、配置快捷键等。

![方法注释](http://blog-1253652709.cos.ap-guangzhou.myqcloud.com/pasteimageintomarkdown/2023-09-24/57318343465500.gif)

![属性注释](http://blog-1253652709.cos.ap-guangzhou.myqcloud.com/pasteimageintomarkdown/2023-09-24/57778844861000.gif)

# Transaction

Translation是一个IntelliJ IDEA的插件，它可以帮助开发者进行翻译和替换文本。该插件支持多种翻译引擎，包括Microsoft
Translator、Google Translate、DeepL Translator等。你可以选择要翻译的文本，然后使用快捷键或右键菜单进行翻译。此外，插件还支持翻译文档、自动识别单词和自动断词等功能。

要安装Translation插件，你可以在IntelliJ IDEA的插件页面搜索"Translation"并进行安装。安装完成后，你可以在IDEA的工具栏或右键菜单中找到Translation插件的功能。

使用Translation插件非常简单。你可以选中要翻译的文本，然后使用快捷键或右键菜单进行翻译。插件会根据你的设置选择合适的翻译引擎，并显示翻译结果。你还可以使用插件的其他功能，如替换文本、翻译文档等。

![简单的翻译操作](http://blog-1253652709.cos.ap-guangzhou.myqcloud.com/pasteimageintomarkdown/2023-09-24/57623950835200.gif)

# .ignore

.ignore插件是一个用于生成.gitignore文件的IntelliJ IDEA插件。.gitignore文件用于指定要忽略的文件和文件夹，这些文件和文件夹在使用Git进行版本控制时不会被跟踪和提交。

使用.ignore插件非常简单。你可以右键单击项目文件夹，选择"New"，然后选择".ignore file"
，即可生成一个新的.gitignore文件。你可以在生成的文件中添加要忽略的文件和文件夹的规则，插件会根据你的选择自动生成相应的规则。

此外，.ignore插件还支持从模板中选择常见的.gitignore规则，以便快速生成.gitignore文件。

安装.ignore插件的方法与安装其他IntelliJ IDEA插件相同。你可以在IDEA的插件页面搜索".ignore"
并进行安装。安装完成后，你可以在IDEA的菜单栏或右键菜单中找到.ignore插件的功能。

.ignore插件可以帮助你更方便地管理.gitignore文件，使你的代码库更加整洁和可维护。如果你经常使用Git进行版本控制，这个插件会对你的工作流程非常有帮助。

![右键指定目录生成即可](http://blog-1253652709.cos.ap-guangzhou.myqcloud.com/pasteimageintomarkdown/2023-09-24/57928871693400.png)

# Atom Material Icons

Atom Material Icons是一个为Atom编辑器设计的图标主题。它为编辑器的文件树、侧边栏和标签栏等部分提供了美观的图标，使用户能够更直观地识别和区分不同类型的文件和目录。

Atom Material Icons的设计灵感来自于Google Material
Design，它采用了简洁、扁平的风格，图标清晰易辨。这个图标主题提供了丰富的图标，包括常见文件类型、文件夹、操作按钮等等，可以根据用户的需要进行自定义和配置。

要安装Atom Material Icons主题，你可以打开Atom编辑器的设置界面，点击"Install"选项卡，然后在搜索框中输入"atom-material-icons"
。在搜索结果中找到对应的主题，点击"Install"按钮进行安装。安装完成后，你可以在编辑器的设置中选择这个主题，并根据需要进行个性化配置。

使用Atom Material Icons主题可以为你的Atom编辑器增添一些视觉上的美感，并且提供更好的文件和目录识别体验。如果你喜欢Google
Material Design的风格，这个主题可能会成为你的首选。

![观察左边目录图标](http://blog-1253652709.cos.ap-guangzhou.myqcloud.com/pasteimageintomarkdown/2023-09-24/58003805426000.png)

# Batch Scripts support

Batch Scripts support是一个用于支持Windows批处理脚本（.bat或.cmd文件）的IntelliJ IDEA插件。使用这个插件，你可以在IDEA中编辑和运行批处理脚本，提高开发效率。

安装Batch Scripts support插件非常简单。你可以打开IntelliJ IDEA的插件页面，搜索"Batch Scripts support"
并进行安装。安装完成后，你可以在IDEA的设置中启用该插件，并进行相关配置。

使用Batch Scripts
support插件，你可以在IDEA中创建和编辑批处理脚本文件。插件提供了语法高亮、代码提示、代码格式化等功能，使你能够更方便地编写和维护批处理脚本。此外，插件还提供了运行和调试批处理脚本的功能，你可以在IDEA中直接运行脚本，并查看输出结果和调试信息。

Batch Scripts support插件还支持在IDEA的终端中运行批处理脚本，你可以方便地执行脚本命令，并查看执行结果。

比如我现在写博客就可以方便执行Hexo相关命令

![](http://blog-1253652709.cos.ap-guangzhou.myqcloud.com/pasteimageintomarkdown/2023-09-24/58118981420300.png)

# Camel Case

# Chinese Language Pack

不多说了。。这个就是官方中文插件

# code glance pro

Code Glance Pro是一个用于IntelliJ IDEA的插件，它在编辑器窗格中显示一个类似于Sublime中的缩略图或总览视图。这个插件可以让你快速滚动代码，跳转到代码的不同部分。Code
Glance Pro在CodeGlance的基础上进行了改进，支持更多功能。

Code Glance Pro插件的主要功能包括：

- 隐藏原始滚动条。
- 右键快速配置。
- 支持标记高亮。
- 支持错误条纹高亮。
- 支持Vcs行高亮。
- 支持光标行高亮。
- 支持语言配色方案。
- 在Glance上快速查看代码。
- 在分割模式下自动计算宽度。
- 使用Ctrl-Shift-G快捷键切换Glance视图。

使用Code Glance Pro插件可以提供更好的代码浏览和导航体验。它可以让你更方便地浏览和编辑代码，快速定位到感兴趣的部分。如果你经常需要处理大型代码文件或项目，这个插件可能会对你的开发效率有所帮助。

你可以在IntelliJ IDEA的插件页面搜索"Code Glance Pro"并进行安装。安装完成后，你可以在IDEA的设置中找到该插件，并进行相关配置。

![](http://blog-1253652709.cos.ap-guangzhou.myqcloud.com/pasteimageintomarkdown/2023-09-24/58313056505900.gif)

# Dto Generator

一键根据JSON生成DTO插件

![](http://blog-1253652709.cos.ap-guangzhou.myqcloud.com/pasteimageintomarkdown/2023-09-24/58863477700200.gif)

# GenerateAllSetter

![](https://raw.githubusercontent.com/gejun123456/intellij-generateAllSetMethod/master/screenshot/generateSetterPlugin.gif)

![](https://raw.githubusercontent.com/gejun123456/intellij-generateAllSetMethod/master/screenshot/generate_the_conveter.gif)

![](https://raw.githubusercontent.com/gejun123456/intellij-generateAllSetMethod/master/screenshot/generate_list_default_value.gif)

。。。好用的插件太多了，下回再聊。。。


