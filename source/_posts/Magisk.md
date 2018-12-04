---
title: Magisk 模块分享
categories:
  - 系统
date: 2018-12-04 08:02:00
tags:
author: 神经元
---

**本文章全部模块可在 [百度云](https://pan.baidu.com/s/112OsDSGCA6iGsHXtB3_YIg) 提取码:n15n 的 Magsik 文件夹中下载**

1. Android O APT-X libraries
在Oreo和Pie上开启蓝牙对APT-X协议的支持
[XDA](https://forum.xda-developers.com/apps/magisk/port-aptx-aptxhd-oreo-8-0-update-jan-t3731151)

2. AOSP Volume Steps Increase
将音量调节级别提高至30
[XDA](https://forum.xda-developers.com/apps/magisk/module-aosp-volume-steps-increase-t3843492)

3. Busybox for Android NDK
Busybox，这个没啥好说的。但是已知bug是这个模块会干扰Magsik Hide的运行，**使添加到其中的所有App闪退**。（Google Play服务会自动被添加到Magisk Hide中）
[XDA](https://forum.xda-developers.com/showpost.php?p=64228091&postcount=420)

4. Camera2 API Enabler
Camera2 API，主要是为了让Google相机可以正常运行。
[XDA](https://forum.xda-developers.com/apps/magisk/module-camera2api-enabler-t3656651)

5. Dolby Digital Plus®
为Oreo和Pie安装杜比全景声音效。
[XDA](https://forum.xda-developers.com/android/software/mm-p-dolby-digital-plus-arise-20181115-t3868192)

6. Global Optimized GPS File Replacer
GPS玄学优化。
[XDA](https://forum.xda-developers.com/mi-5/how-to/step-step-definitive-gps-solution-global-t3695769)

7. GPU Turbo Boost
GPU玄学优化，号称加速75%省电25%，不过心理安慰作用可能更大一些。
[XDA](https://forum.xda-developers.com/apps/magisk/module-gpu-turbo-boost-t3808541)

8. Greenify4Magisk
给绿色守护开启系统集成的特权模式。
[XDA](https://forum.xda-developers.com/apps/magisk/module-greenify4magisk-t3606277)

9. Lawnstep
须配合Lawnchair使用，在Pie上开启Pie风格的上滑最近任务栏和导航栏手势。
[Github](https://github.com/Magisk-Modules-Repo/lawnstep)

10. Magisk Manager for Recovery  Mode (mm)
救砖神器，可以在TWRP中管理Magisk模块。通过在终端中输入以下命令来启动。
    /data/media/mm
[XDA](https://forum.xda-developers.com/apps/magisk/module-tool-magisk-manager-recovery-mode-t3693165)

11. Magisk SELinux Manager
用Magisk切换SELinux状态，不用每次开机改了。
[XDA](https://forum.xda-developers.com/apps/magisk/module-magisk-selinux-manager-t3760042)

12. MagisKHide Props Config
通过更改设备指纹来帮助设备通过SafetyNet检查。
[XDA](https://forum.xda-developers.com/apps/magisk/module-magiskhide-props-config-t3789228)

13. Riru - Core
让 Riru 模块们进入应用进程或系统服务进程并执行他们的代码，目前用途见下文。
[Github](https://github.com/RikkaApps/Riru)

14. Riru - Location Report Enabler
启用Google位置报告，必须安装Riru - Core。
[Github](https://github.com/RikkaApps/Riru/tree/master/riru-core)

15. Setting summary text file
修复 当语言为中文时，所有基于AOSP的ROM的设置的高级显示异常 的问题。

16. Single User Mod
禁用多用户功能并删除来宾账户。
[XDA](https://forum.xda-developers.com/apps/magisk/module-single-user-mod-t3639486)

17. sleek+筑紫字体 for N+
本文作者制作，在Nougat以上的系统中替换字体为sleek+筑紫。
[酷安](https://www.coolapk.com/feed/5091727)

18. Wifi Bonding (Qualcomm)
在高通设备上以40MHz的运行的2.4GHz / 5.0GHz的无线网络连接，其实我也不知道具体有啥用，反正安了没坏处
[Github](https://github.com/Magisk-Modules-Repo-CN/magisk-wifi-bonding/blob/master/README.md)