---
title: '笔记 - 崩坏: 星穹铁道 和 原神的触控代码'
published: 2025-01-16
description: ''
image: ''
tags: [Game, Cloud Game, Mihoyo, 游戏, 云游戏, 米哈游]
category: '笔记'
draft: false 
lang: 'zh_CN'
---

<!-- # 笔记 - 崩坏: 星穹铁道 和 原神的触控代码 -->

> 注意:
> 触控代码只适用于 PC 上的游戏客户端

触控代码可用于搭建云游戏服务，如果嫌麻烦可以使用 [胡桃启动器](https://hut.ao/zh/) 自带的 [启动参数](https://hut.ao/zh/features/game-launcher.html#%E5%90%AF%E5%8A%A8%E5%8F%82%E6%95%B0) 设置云游戏

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