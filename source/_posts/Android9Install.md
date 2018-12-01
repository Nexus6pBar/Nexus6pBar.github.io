---
title: Android9.0通用安装教程
categories:
  - 刷机
date: 2018-12-01 17:12:00
tags:
author: Gospodaru
---


Android 9.0通用安装教程
-----------

**注意：安装之前务必退出谷歌账号**

    准备文件:
    
    -   Rom卡刷包
    
    -   谷歌套件(GAPPS)
    
    -   Magisk卡刷包(用于ROOT)
    
    -   platform-tools（使用方法参考heart大佬的教程）
    
    -   确保已刷入第三方REC（参考heart大佬教程）

>   **注意:Pe,Aex需要刷入特定Rec**

>   下载地址: :https://pan.baidu.com/s/112OsDSGCA6iGsHXtB3_YIg 提取码:n15n

>   Recovery→recovery(special).img

1.确保手机BL锁已解，并且打开OEM解锁和USB调试，并对计算机授权。

2.使用platform-tools下的adb.exe，输入adb reboot Recovery

{% asset_img enterRec.png 进入REC1 %}

或者手机关机，然后按住电源键与音量-键进入BL模式。

3.连按两下音量- ，再按一次电源键选中Recovery mode。

{% asset_img Recmode.png 进入REC2 %}

4.等待片刻则会进入REC模式

{% asset_img Recmenu.png 进入菜单 %}

5.点击 清除 → 高级清除
，四清，确认（如果刷入的是特定Rec，执行完这部后先重启Rec）。

{% asset_img Fullwipe.png 四清 %}

{% asset_img progess.png 进程 %}

6.返回到菜单，使用电脑将Magisk卡刷包(Magisk-v17.2.zip)，Rom卡刷包(aicp_angler_p-14.0-NIGHTLY-20181122.zip)，谷歌套件(open_gapps-arm64-9.0-stock-20181124.zip)拖入手机存储。

{% asset_img File.png 移动文件 %}

7.点击安装，选中aicp_angler_p-14.0-NIGHTLY-20181122.zip，然后添加更多刷机包将其它两个选上，确定，然后耐心等待。

8.完成后返回主菜单，选中清除，点击格式化Data分区，输入yes，然后返回清除，双清。

{% asset_img Format.png 格式化Data %}

{% asset_img Reset.png 双清 %}

9.完成后可以重启（如果第一次启动出现自动重启，请耐心等待，属于正常现象）
