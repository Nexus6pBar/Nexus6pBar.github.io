---
title: 干掉淘宝和QQ自动WebView核心
categories:
  - 软件
date: 2018-12-09 11:21:35
tags:
author: sora
---

## 引言

- 阿里系的应用因为其臃肿卡顿饱受诟病，究其症结，淘宝、支付宝、闲鱼等阿里系应用都大量应用了WebView

- 提到WebView，其在安卓中的应用还是非常广泛的。提到阿里的WebView，就不得不提到UC，UC浏览器在塞班系统上表现无敌，然而在Android上表现平平，在加入阿里系之后完全跻身“毒瘤”行列。

- 淘宝、闲鱼、支付宝为什么这么大？在查看data文件夹后不难发现它们都内置了一个30M的UC WebView组件，这个组件相对于目前主流手机的Android Webv（MIUI10系统WebView已经基于Chrome 62），表现是比较差的

- 让这些软件直接调用系统WebView，能够降低RAM占用，同时提供更好的浏览体验

## 操作
以下操作需要获取Root权限

## 淘宝UC核心路径
> /data/data/com.taobao.taobao/app_ucmsdk/updates/(数字)/(数字)/lib/libwebviewuc.so

## 闲鱼UC核心路径
> /data/data/com.taobao.idlefish/app_ucmsdk/updates/(数字)/(数字)/lib/libwebviewuc.so

以上两者直接删除30M的libwebviewuc.so既可

## 支付宝UC核心路径
> /data/data/com.eg.android.AlipayGphone/app_h5container

将该文件夹权限设置为000（去掉所有权限的勾），然后删除该文件夹下所有文件既可

## 腾讯系应用
对于腾讯系的应用（QQ\微信）其采用的是QQ浏览器X5内核，基于Chrome 57，如果你的手机WebView版本更高，可以考虑关闭X5内核

在QQ/微信中访问 [http://debugtbs.qq.com](http://debugtbs.qq.com)

选择右下角禁用内核既可

结语
内核检测工具

[https://ie.icoa.cn/](https://ie.icoa.cn/)

[http://liulanmi.com/](http://liulanmi.com/)

​禁用软件自带的WebView可能造成部分不兼容的问题，腾讯系重新打开X5内核、阿里重新覆盖安装一次既可