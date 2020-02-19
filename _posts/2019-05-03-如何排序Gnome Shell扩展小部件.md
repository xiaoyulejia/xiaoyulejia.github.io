---
layout:     post
title:      如何排序Gnome Shell扩展小部件
date:       2019-05-03
author:     Limexb
header-img: img/home-bg-o.jpg
catalog: true
tags:
    - Linux
---

![我的Shell面板](https://s2.ax1x.com/2020/02/19/3ECK00.png)

## 首先，找文件
要找到要更改的扩展的相应文件。
一般她躲在这里O(∩_∩)O哈！```~/.local/share/gnome-shell/extensions```。

## 第二，改文件
然后进入扩展目录并使用任何文本编辑器打开extension.js。
使用编辑器中的搜索功能找到这行```function enable()```。
这个函数里面通常有一行```Main.panel.addToStatusArea('NAME', _OTHERNAME, NUMBER, LEFT/CENTER/RIGHT);```或者```Main.panel.addToStatusArea('NAME', _OTHERNAME);```。

其中```POSITION```对应着Shell面板上的三个区域。
#### ```POSITION```可能的值
Activities|Date|Other icons
--|--|--
left|center|right
只要修改```POSITION```，就能让Shell扩展小部件在Shell面板的三个区域星际跳跃啦\(≧▽≦)/。

改完你可能会发现，这样只能控制Shell扩展小部件在Shell面板上的区域，并不能控制它在哪个位置，于是你需要```NUMBER```，它定义子面板内图标的顺序。


#### ```NUMBER```可能的值
值|解释
--|--
0|我才不在乎自己在哪呢！（不在乎图标位置）
负值|劳资要从右侧开始！！<(ˉ^ˉ)>（图标从右侧开始排列）
正值|劳资要从左侧开始！！<(ˉ^ˉ)>（注意，较高的值将位于右侧）

改完记得保存哦，亲(づ￣3￣)づ╭❤～

## 最后，重启Gnome Shell
按下```Alt```+ ```F2```
输入```r```
轻轻按下你键盘上的```Enter```并开始祈祷。