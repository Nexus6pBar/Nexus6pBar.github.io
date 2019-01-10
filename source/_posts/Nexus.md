---
title: 身为小白你必须会的知识:从解锁到刷机
categories:
  - 刷机
date: 2018-12-01 22:25:00
tags:
author: HEART
---

##### 1.1 解锁

在Nexus6P遇到各种问题，卡在开机界面无法进入系统，也就是变砖，这时可以进入bootloader进行刷机来救砖，但进入bootloader操作的前提是要解锁，而从Nexus6开始，Google加入了OEM锁来管住bootloader锁，所以要先解OEM锁，再解bootloader锁。

##### 1.2 解OEM锁

解OEM锁也是非常简单的，只要打开开发者选项（在设置-系统-关于手机里面狂点版本号，如图：

{% asset_img 1.jpg %}

系统会提示你 您已处于开发者模式 ），然后在开发者选项找到OEM解锁，如图：

{% asset_img 2.jpg %}

这样OEM锁就解锁完成。

##### 1.3 解bootloader锁

解好OEM锁后把手机关机，长按音量-和电源键，手机会出现一个倒地的机器人，这时你已经进入bootloader模式，接下来用数据线连接电脑，然后开始电脑操作。

###### 1.3.1配置platform tools

首先你得下载Platform tools工具包

下载地址：[百度云](https://pan.baidu.com/s/112OsDSGCA6iGsHXtB3_YIg) 提取码:n15n (PlatformTools)

解压这个压缩包，解压后会有一个文件夹，点开后再点开里面的文件夹，然后就会看到这些：

{% asset_img 3.png %}

接着开始配置环境变量，首先右键计算机（此电脑）然后点击属性，在这个窗口找到高级系统设置

{% asset_img 4.png %}

接着找到环境变量

{% asset_img 5.png %}

复制platform tools的文件夹目录

{% asset_img 7.png %}

选择Path，点击编辑，再新建一个变量  
{% asset_img 8.png %}  
{% asset_img 24.png %}

粘贴刚才复制的文件地址

{% asset_img 9.png %}

确定，这样adb的环境变量就配置好了，以后不要移到或删除这个文件夹。

对于Linux及MacOS系统的用户，我们默认您已经或可以通过搜索引擎自行掌握了相关环境的配置，故省略。如有需要，请与站点管理员[联系](/about)

###### 1.3.2开始解锁

打开Windows命令提示符，在打开命令窗口之后，在窗口里输入：

    fastboot flashing unlock

然后回车，手机上将会出现这个提示：

{% asset_img 6.png %}

音量键选择yes然后电源键确认，解锁完成。

注意：解锁会清除手机所有的数据，请及时备份和退出Google账户

##### 2.1 线刷官方包

解锁成功后，如果不是硬件上的损坏，都可以利用线刷官方包来解决，首先手机进入bootloader

电脑下载官方包，链接：

[官方包](https://developers.google.cn/android/images)

* 方法一：

下载合适的版本之后解压，解压完成后打开文件夹，有以下文件：

{% asset_img 10.png %}

继续解压里面的压缩包，如图：

{% asset_img 11.png %}

移动文件夹里的文件到上一个目录

{% asset_img 12.png %}

双击里面的flash-all.bat，接着开始自动线刷，期间不要移动手机，电脑的命令窗口也不要乱动。

* 方法二：

如果按照方法一的教程出现报错，那么可以试试方法二，首先在刷机

包文件夹里按shift+鼠标右键，选择在此处打开PowerShell（命令窗口）如图：

{% asset_img 13.png %}

打开后在命令窗口输入（输入后回车）：

~~~bash
fastboot flash bootloader bootloader-angler-angler-03.81.img //不同的刷机包文件名不同)
fastboot reboot bootloader
fastboot flash radio radio-angler-angler-03.88.img //不同的刷机包文件名不同
fastboot flash boot boot.img
fastboot flash recovery recovery.img
fastboot flash system system.img
fastboot flash vendor vendor.img
fastboot reboot
~~~

**线刷完成后手机会重启**

###### 2.2 安装手机驱动

如果手机连接电脑执行命令出现这样的提示：

{% asset_img 16.png %}

在检查好手机是否已经正确用数据线连接电脑并且进入bootloader模式后，如果还出现上述情况，那么就是驱动未正确安装，所以要安装手机驱动。

1.  下载手机驱动

2.  解压到电脑（最好是你可以记住的位置）

3.  右键此电脑（计算机），点击属性-设备管理器

{% asset_img 17.png %}

{% asset_img 18.png %}

{% asset_img 19.png %}

4.找到设备，一般是：nexus6p，Android Device，bootloader等等

右键设备，选择更新驱动程序-浏览我的计算机以查找驱动程序

{% asset_img 20.png %}

{% asset_img 21.png %}

然后找到你刚才下载并解压后的文件夹，点击安装。

##### 3.1 卡刷（此教程用到的rom是：Resurrect Remix OS 6.1）

卡刷是把ROM存放在手机里，进入recovery模式进行刷机，recovery模式就是手机的恢复模式（相当于电脑的WindowsPE），首先刷入第三方的recovery，比如twrp（Team
Win Recovery Project）：

进入bootloader，然后电脑下载文件，打开命令提示符，输入：

    fastboot flash recovery

把下载好的文件拖入命令窗口后回车，如图：

{% asset_img 15.png %}

手机bootloader按音量键出现Recovery
Mod时按电源键进入recovery模式（注意：不能重启进入官方rom，不然会恢复成官方recovery，twrp等于白刷。）

然后会出现一个界面，直接滑动就好。

滑动之后就是twrp的主界面了，接着在手机上点击wipe（清除），选择

{% asset_img 22.png %}

这几个选项（俗称4清）

然后把手机连接电脑，电脑出现手机的内部储存共享空间后把卡刷包复制进去，退回到主界面，点击install（安装），找到刚才的卡刷包，点击后滑动，开始刷入，开始等待。
