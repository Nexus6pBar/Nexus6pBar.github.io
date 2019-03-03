---
title: 老司机带你优化Nexus 6p
categories:
  - 软件
date: 2019-03-03 17:03:59
tags:
author: sora
---

 # 系统优化
　　看到群里面很多人说手机卡，发热，但又不能每次都在线一部部的交吧，故写篇教材
　　优化前提首先你要有root，这里推荐使用Magisk，因为稍候会用到一些模块（如果不会刷入的可以看我们上一篇教程）

## 优化1（刷入模块,记得刷入后重启哦😝）
首先我们先刷入调度模块viper调度

[百度云](https://pan.baidu.com/s/112OsDSGCA6iGsHXtB3_YIg) 提取码:n15n （优化教程/viper调度（酷安ID：TSU守望者）.zip）  

群里还有很多人使用gapps的，耗电高怎么办没问题，使用模块让它乖乖打盹
这里推荐 Universal GMS Doze

[百度云](https://pan.baidu.com/s/112OsDSGCA6iGsHXtB3_YIg) 提取码:n15n （优化教程/Universal_GMS_Doze-v1.6.1_(LST01F,_Mar_2019).zip）

### 这里使用Magisk刷入，当然你也可以用rec刷入（下面是刷入方法）
先打开面具🎭，如图
{% asset_img 1.png %}
然后滑出侧栏，如图
{% asset_img 2.png %}
再点击模块，如图
{% asset_img 3.png %}
再点击加号，找到要刷入的模块，点击模块，就会看到如图，这里是以viper调度为例
{% asset_img 4.png %}
最后点击关闭刷入其他模块，或者点击重启就大功告成了

## 优化2
使用黑域这里推荐群里面的版本

[百度云](https://pan.baidu.com/s/112OsDSGCA6iGsHXtB3_YIg) 提取码:n15n （优化教程/黑域_3.0.7.apk）

　　
进入黑域后首先会看到这个画面不用管，直接滑动到使用，授予root权限即可
{% asset_img 5.png %}
{% asset_img 6.png %}
{% asset_img 7.png %}
{% asset_img 8.png %}

### 下面就是如何设置黑域了（这可能是最详细的黑域使用教程）
先点击右上角三个点
{% asset_img 9.png %}
然后按图片将设置里面的开关打开或关掉
{% asset_img 10.png %}
{% asset_img 11.png %}
然后回到黑域主界面
{% asset_img 12.png %}
先随便点一个图标（记住是图标，不是文字）
{% asset_img 13.png %}
然后点击反选
{% asset_img 14.png %}
会显示如图
{% asset_img 15.png %}
接着把反选之后没有选择的图标点一下，会显示如图
{% asset_img 16.png %}
再点击
{% asset_img 17.png %}
如果你不想让黑域杀掉一些应用，想使他长驻后台可以加入白名单
如图所示
{% asset_img 18.png %}
{% asset_img 19.png %}

### 黑域还有一个冻结的功能，冻结你不常使用的功能
有了它你不用再装冰箱，小黑屋等冻结软件，可以说是非常强大了
点击需要冻结的app，这次就不要点图标，要点图标以外的地方，然后选择冻结就行了，如图
{% asset_img 20.png %}

### 黑域还有一个很特殊的功能，就是无需电脑使用adb命令

只沉浸状态栏： 
```bash
adb shell settings put global policy_control immersive.status=*
```
　
只沉浸导航栏：
```bash 
adb shell settings put global policy_control immersive.navigation=*
```
　　
沉浸导航栏和状态栏： 
```bash
adb shell settings put global policy_control immersive.full=*
```

恢复官方默认： 
```bash
adb shell settings put global policy_control null
```

单独控制某一个app不沉浸，比如以下代码设定google实时界面不沉浸，其他程序沉浸：
```bash
adb shell setting put global policy_control immersive.navigation=apps,-ch.deletescape.lawnchair.ci
```

例如这些指令，使用前删掉adb shell就可以使用黑域使用了
```bash
settings put global policy_control immersive.navigation=apps,-ch.deletescape.lawnchair.ci,-com.google.android.GoogleCamera,-com.google.android.inputmethod.latin
```

好了黑域教程到此为止了

## 优化3
　　你还在怕app窃取你的隐私吗？关了权限无法打开app的情况吗？还怕毒瘤软件在后台长期运行，导致手机卡卡的吗？有了它你就就不必担心，它就是神器 App ops，一款系统给了权限，但只要它不给权限照样无法读取你的权限的管理应用，麻麻再也不用担心隐私泄露了

### 使用方法
系统里面给应用权限，app ops拒绝权限这样应用就无法使用该权限了

有人要问了，我需要这个权限，但只想在使用的时候用到它，而不想让它在后台使用该怎么办？没问题，app ops加入了这个解决方案

### 以淘宝为例
选择前台时允许就可以完美解决这个问题，如图所示
{% asset_img 21.png %}
在使用安卓9.0的时候我们还可以用appops可以加以限制后台，让毒瘤无法在后台肆无忌惮运行，压死毒瘤

### 同样以淘宝为例子
滑到权限最下面，点击在后台运行，选择严格限制，如图所示
{% asset_img 22.png %}　　