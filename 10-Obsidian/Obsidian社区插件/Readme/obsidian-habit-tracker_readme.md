---
uid: 20230803212514
title: Obsidian 插件：【Readme】Habit Tracker
tags: ['日期相关', '界面相关', 'obsidian插件', 'readme']
description: 创建一个简单的日历视图，用于记录和显示你的笔记活动记录
author: AI
type: readme
draft: false
editable: false
modified: 20230101000000
---

# Obsidian 插件：Habit Tracker

> [!Note] 插件名片
> - 插件名称：Habit Tracker
> - 插件作者：duo
> - 插件说明：创建一个简单的日历视图，用于记录和显示你的笔记活动记录
> - 插件分类：['日期相关', '界面相关', 'obsidian插件', 'readme']
> - 项目地址：[点我访问](https://github.com/duoani/obsidian-habit-tracker)
> - 国内下载地址：[下载安装](https://pkmer.cn/products/plugin/pluginMarket/?obsidian-habit-tracker)

## 概述

创建一个简单的日历视图，用于记录和显示你的笔记活动记录

![Habit Tracker](https://cdn.pkmer.cn/covers/obsidian-habit-tracker.PNG!pkmer)

> [!tip] 原文出处
> 
>下面自述文件的来源于 [Readme](https://ghproxy.net/https://raw.githubusercontent.com/duoani/obsidian-habit-tracker/master/README.md)
> 

---

## Readme(翻译）

下面是 [[obsidian-habit-tracker]] 插件的自述翻译



## Obsidian习惯追踪插件

这个插件为[Obsidian](https://obsidian.md/)创建了一个简单的月视图，用于可视化您的打卡记录。

![](./screemshot.png)

如何操作
要显示上面的视图，只需创建一个代码块并输入：

~~~
```habitt
[month:2021-06]
(1,💮)(2,💮💮)(3)(5)(6)(7)(9, ⚽)(10, 🏄)(12)(18,💮💮💮)(22,🏆)(28,Pass) 
```
~~~

* `[month:YYYY-MM]`：要显示的月份
* `(date_num, tag)`：您想要打卡的日期（`date_num`），并在其中添加一个标签（`tag`）。如果缺少`tag`，例如`(12)`，则该日期将被赋予默认标签`✔️`。
* `[width: css_width]`：将月视图表格限制为`css_width`，例如`[width: 50%]`，`[width: 500px]`

### 富文本
有些人喜欢插入富文本（例如链接或图片）。自从v1.0.4版本以来，Habit Tracker插件添加了一个新的配置项`启用HTML`来激活HTML解析。**出于安全原因，该配置默认为“关闭”。**

插入网址链接：
~~~
```habitt
(1, )
```
~~~

插入Vault中的其他笔记（使用Obsidian URL）：
~~~
```habitt
(1, )
```
~~~
了解更多关于[Obsidian URL](https://help.obsidian.md/Advanced+topics/Using+obsidian+URI)的信息。

插入网络图片：
~~~
```habitt
(1, <img src="https://www.xyz.com/img.jpg" />)
```
~~~
目前，在Obsidian中我们无法使用`<img />`标签链接本地图片。参见[Does ANY HTML work in Obsidian w/local files? - Resolved help - Obsidian Forum](https://forum.obsidian.md/t/does-any-html-work-in-obsidian-w-local-files/8000)。

## 安装

您可以通过Obsidian中的Community Plugins选项卡安装插件。只需搜索“Habit Tracker”。



