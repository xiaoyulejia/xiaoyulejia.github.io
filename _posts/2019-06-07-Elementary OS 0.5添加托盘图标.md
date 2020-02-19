---
layout:     post
title:      Elementary OS 0.5添加托盘图标
#subtitle:   Elementary OS更新Plank
date:       2019-06-23
author:     Limexb
header-img: img/home-bg-o.jpg
catalog: true
tags:
    - Elementary OS
    - Linux
---

Elementary OS颜值很高，但它有个反人类的设计（取消系统托盘）

本文提供一种解决方法，可以给Elementary OS添加系统托盘

### 安装插件
>$ sudo add-apt-repository ppa:yunnxx/elementary
>
>$ sudo apt update
>
>$ sudo apt install indicator-application wingpanel-indicator-ayatana

### 编辑配置
你需要编辑一个文件（在这里，我使用nano，你随意）

>sudo nano /etc/xdg/autostart/indicator-application.desktop

找到这一行

>OnlyShowIn=Unity;GNOME;

在后面添加Pantheon;

>OnlyShowIn=Unity;GNOME;Pantheon;



安装完需要重启一下，回来应该就能看见托盘图标了(*^__^*) 嘻嘻……

![效果图](https://s2.ax1x.com/2020/02/19/3EnsOO.png)
