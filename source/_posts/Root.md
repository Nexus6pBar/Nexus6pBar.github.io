---
title: 怎么获取Nexus6p的root权限
categories:
  - 系统
date: 2019-02-05 20:16:59
tags:
author: HEART
---

Root是Android手机的进阶玩法（即获取最高权限）
教程分两块：
### 1  Android6.0.0-7.1.2的用户
1.下载SuperSU的卡刷包并放入手机内置储存的根目录
2.线刷TWRP（已经刷入的忽略）
3.从Bootloader进入TWRP，或者在关机状态下，按住电源键+音量上键进入TWRP
4.点击Install，找到并点击SuperSU的zip格式卡刷包
5.滑动滑块刷入
6.重启手机
### 2  Android8.1.0-9.0.0的用户
1.下载Magisk的卡刷包并放入手机内置储存根目录
2.线刷TWRP（已经刷入的忽略）
3.从Bootloader进入TWRP，或者在关机状态下，按住电源键+音量上键进入TWRP
4.点击Install，找到并点击Magisk的zip格式卡刷包
5.滑动滑块刷入
6.重启手机

*注意：Android9.0.0的用户如果刷入Magisk之后启动器里没有Magisk Manager的话请去下载并安装*
