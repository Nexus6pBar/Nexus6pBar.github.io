---
title: Android 9.0 通用安装教程
categories:
  - 刷机
date: 2018-12-08 14:12:00
tags:
author: Gospodaru
---


**注意：安装之前务必退出谷歌账号**

准备文件:

*  Rom卡刷包（这里以Pe为例）

*  谷歌套件(GAPPS)

*  Magisk卡刷包(用于ROOT)

*  platform-tools（使用方法参考heart大佬的教程）

*  Rec文件

请务必刷入最新支持FBE的Rec

下载地址：[百度云](https://pan.baidu.com/s/112OsDSGCA6iGsHXtB3_YIg) 提取码:n15n

Recovery→recovery(special)→recovery.img

1.确保手机BL锁已解，并且打开OEM解锁和USB调试，并对计算机授权。

2.进入BL模式，手机关机，然后按住电源键与音量-键进入BL模式。

将recovery拖入platform-tools下的文件夹，使用platform-tools下的adb.exe(按住Shift右击文件夹空白处,单击在此打开命令窗口)
。

{% asset_img 7f3cd15638e474b5eb7f4f9a86abcda7.png  %}

输入

```bash
fastboot flash recovery recovery.img
```

回车

{% asset_img 7a19b3c5a0d0cb0e9644daf724bc83c7.png  %}

{% asset_img 316a9c6cd4aa35c0e75581a63bf8e037.png  %}

3.按两下音量- ，再按一次电源键选中Recovery mode。

{% asset_img 2f0c9f891e54a245cb7873a7cbfb73a3.png  %}

{% asset_img 0221884b78d4c024f169837fd4a451b2.png  %}

4.点击Wipe，然后点击Format Data,输入yes确认

{% asset_img 3ec63a9b1fee1d9e07f3df49471a10e7.png  %}

{% asset_img 4afa212236bcff824e7e3aa1b951f1fc.png  %}

{% asset_img 4cc1b6035eb773af42bdb67f79a4f546.png  %}

5.完成后返回Rec主菜单，点击Reboot → Recovery → 滑动以确认。

{% asset_img 0221884b78d4c024f169837fd4a451b2.png  %}

{% asset_img 9c301251a6141cc5e4ce8c4072ed60e5.png  %}

6.重启再点击 Wipe → Advanced Wipe → 全部选上 → 滑动滑块以确定，完成后返回Wipe菜单

{% asset_img 708b7861f35807e953f8568bd3b3ca9f.png  %}

{% asset_img 0d7e81d8d893b7ba17c0a9179add0f61.png  %}

7.重启后来到菜单，单击 Mout，选中一下几个，然后返回菜单

{% asset_img 51c901078133b6dfdde3e7427e41cca3.png  %}

8.将Rom卡刷包 PixelExperience_angler-9.0-20181205-1457-OFFICIAL，Makisk卡刷包 Magisk-v17.2拖入手机存储中的TWRP文件夹

{% asset_img dfaeaca51b65966e6c490326126f36f4.png  %}

9.单击Install,先选中Rom卡刷包PixelExperience_angler-9.0-20181205-1457-OFFICIAL，然后点击Add more Zips选中Magisk卡刷包，滑动确定开始刷入。

{% asset_img 0be9467f6963a7d4cdc696737ff14902.png  %}

{% asset_img 353fc10dfb64b23209c55fdb4aeee7eb.png  %}

{% asset_img 7d77bb047abd87a69dc37a1c80f413b2.png  %}

10.完成，重启等待即可
