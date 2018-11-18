---
title: Bmap等在9.0闪退的分析及解决
categories:
  - 软件
date: 2018-11-18 22:19:00
tags:
author: 神经元
---

###### Q:   
Bmap等软件在Android Pie上闪退
{% asset_img log.jpg 闪退时的日志 %}

###### A: 
Bmap等软件使用了(辣鸡)腾讯乐固，而腾讯乐固使用的 Dexfile API已被Google在API 26弃用，软件的target API高于26时，可能产生各种难以预料的结果。在此也提醒各位开发者选择加固时注意此问题。  
关于此问题的更多内容，请参阅 [Dexfile｜Android Developers](https://developer.android.google.cn/reference/dalvik/system/DexFile)

解决方案：可以通过简单的去壳并重新打包来使这些软件在Pie上正常工作，具体方法请自行研究。  
对于Bmap，借助于 琴梨梨 大佬的帮助，本人已将最新(也是最后一版)Bmap脱壳并重新打包签名。
下载地址：[百度云](https://pan.baidu.com/s/1oTfAszsnyOenUrerBFt66g) 密码：lods  
**本发布仅用于个人学习交流，请自觉遵守相关法律法规，尊重原作者的劳动成果。在此特别感谢原作者 gfuil 开发本软件所付出的劳动和对本破解的支持与理解。**