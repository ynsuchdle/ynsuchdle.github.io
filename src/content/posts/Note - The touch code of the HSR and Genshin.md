---
title: Note - The touch code of the HSR and Genshin
published: 2025-01-16
description: 'Note'
image: ''
tags: [Game, Cloud Game, Mihoyo, 游戏, 云游戏, 米哈游]
category: ''
draft: false 
lang: 'zh_CN'
---

# 笔记 - 崩坏: 星穹铁道 和 原神的触控代码

> 注意:
> 触控代码只适用于 PC(Windows) 上的游戏客户端 (Mac 未测试)

触控代码可用于搭建云游戏服务

## 崩坏:星穹铁道

### 一. 找到游戏主程序

1. 先打开游戏主程序

2. 游戏启动成功后按 `Ctrl + Alt + Delete` 键调出任务管理器

3. 在任务管理器找到名为 `Star Rail` 的进程，右键进程，点击 打开文件所在位置

![任务管理器](https://cdn.jsdelivr.net/gh/ynsuchdle/Resources@main/images/post/2025-01-16_01/2025-01-16-22-10-11.png)

### 二. 创建游戏主程序的快捷方式

1. 右键找到的游戏主程序 StarRail.exe，点击 发送到 --> 桌面快捷方式

![创建快捷方式](https://cdn.jsdelivr.net/gh/ynsuchdle/Resources@main/images/post/2025-01-16_01/2025-01-16-23-26-34.png)

1. 在桌面找到新建的快捷方式，右键快捷方式，点击 属性，弹出文件属性窗口

![属性窗口](https://cdn.jsdelivr.net/gh/ynsuchdle/Resources@main/images/post/2025-01-16_01/2025-01-16-23-34-44.png)

3. 在属性窗口的目标输入框内容后加入以下字符串，点击 应用 --> 确定

```
-platform_type CLOUD_WEB_TOUCH -graphics_setting eyJGUFMiOjYwfQ==
```

![触控代码](https://cdn.jsdelivr.net/gh/ynsuchdle/Resources@main/images/post/2025-01-16_01/2025-01-17-00-23-37.png)

4. 双击打开快捷方式预览结果

![预览1](https://cdn.jsdelivr.net/gh/ynsuchdle/Resources@main/images/post/2025-01-16_01/2025-01-17-00-34-02.png)

![预览2](https://cdn.jsdelivr.net/gh/ynsuchdle/Resources@main/images/post/2025-01-16_01/2025-01-17-00-36-54.png)

![预览3](https://cdn.jsdelivr.net/gh/ynsuchdle/Resources@main/images/post/2025-01-16_01/2025-01-17-00-38-44.png)

## 原神

原神 的操作与 崩坏: 星穹铁道 的操作时类似的，只需要修改下触控代码:

```
use_mobile_platform -platform_type CLOUD_THIRD_PARTY_MOBILE
```