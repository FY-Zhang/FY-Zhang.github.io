---
layout:     post   				    # 使用的布局（不需要改）
title:      Final Project 制作过程				# 标题 
subtitle:   I-ACG #副标题
date:       2018-12-27 				# 时间
author:     FY_Zhang 						# 作者
header-img: img/Girl-Night.JPG 	#这篇文章标题背景图片
catalog: true 						# 是否归档
tags:								#标签
    - 编程
---
# Final Project

这是我编写的第一个大型程序，集中敲了三天半代码，后来又断断续续增加了一些页面。


本次制作主要参考了<a href = "https://lolico.moe/" target = "_blank">神代綺凜の萌化小基地</a>、<a href = "http://www.runoob.com/" target = "_blank">菜鸟教程</a>、<a href = "http://www.w3school.com.cn/index.html" target = "_blank">W3school</a>，以及其他的一些博客。

美术不好的我制作网页最头疼的地方就是 CSS，由于是期末作业，所以模板什么的不能找，那就借鉴一下别人的吧！于是找到了神代绮凛的 Blog，照着它的样式、颜色做了一个网页出来。虽然由于技术原因，未能将他的 Blog 完美重现，但依然解决了我最为头疼的问题。

![好看就行了，管它像不像呢 (￣▽￣)"](https://raw.githubusercontent.com/FY-Zhang/FY-Zhang.github.io/master/img/FinalProject/HomePage-Contrast.JPG)

做完这些基础的 HTML 页面后，我开始制作真正需要 PHP 的页面，就是上方那一条的右边四个按钮。

我首先做的是 "Animation" 页面，因为我要在这个页面中显示出动漫的详细信息，所以需要用到数据库。这里我为了在表中存入中文，参考了<a href = "https://www.jb51.net/article/147131.htm" target = "_blank">mysql中插入表数据中文乱码问题的解决方法</a>，为了更方便地往数据库中存入数据，参考了<a href = "https://blog.csdn.net/qq_36832411/article/details/76619663" target = "_blank">如何使用mysql导入txt数据</a>。

![动画信息数据库](https://raw.githubusercontent.com/FY-Zhang/FY-Zhang.github.io/master/img/FinalProject/Database-txt.GIF)

建立完数据库后，我利用 PHP 连接数据库，然后读取里面的动漫名(Name)和图片地址(Cover)，然后将它们平铺在网页上。有两季及以上的动画自动在名字后面加上第几季，只有一季的只显示动画名，这里我用非常简单粗暴的 for 循环判断是否只有一季，肯定有更好的办法，但我暂时还想不到。于是，"Animation" 页面就做成了这个样子：

!["Animation" 页面](https://raw.githubusercontent.com/FY-Zhang/FY-Zhang.github.io/master/img/FinalProject/Animation.jpg)

接下来是登录、注册和登出，我参考了<a href = "https://www.cnblogs.com/leinov/p/3745401.html" target = "_blank">php注册登录系统</a>和<a href = "https://zhidao.baidu.com/question/1882548854151467788.html" target = "_blank">php判断用户是否登录</a>，稍微改了改里面的代码，然后作为自己的，很轻松就弄出来了。登出的话我将它设定为点击名字后跳转到一个页面，然后那里有清除 SESSION 的代码。

![注册和登录](https://raw.githubusercontent.com/FY-Zhang/FY-Zhang.github.io/master/img/FinalProject/Login-Signup.jpg)

