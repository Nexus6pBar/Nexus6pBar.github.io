# BaiduNexus6pBar.github.io  
![](https://travis-ci.org/Nexus6pBar/Nexus6pBar.github.io.svg?branch=source)

-------

这是一个由百度Nexus6P吧官方群部分dalao维护的关于Nexus6P的教程网站。  
source分支：网站源码  
master分支：Hexo编译后的网站  
 ** 警告：除非您完全清楚您正在做什么，否则您不应该直接手动修改master分支，该分支应由Hexo编译后自动更新。** 
    
-------

### 开始工作  
这个网站基于Hexo构建，而Hexo依赖Node.js环境。请在您的计算机上安装Node.js并参考相关教程将其加入环境变量。  
[Download｜Node.js](https://nodejs.org/en/download/)  

下载项目并安装Hexo  
```bash
$ git clone https://Nexus6pbar/Nexus6pBar.github.io.git -b source
$ cd ./Nexus6pBar.github.io
$ npm install
```

使用下面这个命令对项目进行编译  
```bash
$ hexo g
```

要预览编译后的网站，请使用  
```bash
$ hexo s
```  
这将在您的电脑上运行一个本地的HTTP服务器，默认端口为4000。也就是说，在浏览器中访问[localhost:4000](localhost:4000)

如果您拥有足够的权限，可以在修改后提交commit并push到source分支，Travis-CI将自动编译网站并发布。**Hexo deploy已弃用**

更多关于Hexo的使用帮助请参阅官方网站 [Hexo](http://hexo.io/zh-cn)  
我们使用 [Material](https://github.com/viosey/hexo-theme-material) 主题。对于开发人员，此主题的更多帮助在 [Material Theme](https://neko-dev.github.io/material-theme-docs/#/)

-------

### 联系我们  
QQ群：740661764

-------

### License  
###### 对于本网站所有原创内容，如无特殊声明使用 CC BY-SA 4.0 License  
> This work is licensed under the Creative Commons Attribution-ShareAlike 4.0 International License. To view a copy of this license, visit http://creativecommons.org/licenses/by-sa/4.0/ or send a letter to Creative Commons, PO Box 1866, Mountain View, CA 94042, USA. 
  
###### Hexo ([https://github.com/hexojs/hexo](https://github.com/hexojs/hexo))
>Copyright (c) 2012-2017 Tommy Chen
>Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions: 
>The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software. 
>THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
  
###### Material ([https://github.com/viosey/hexo-theme-material](https://github.com/viosey/hexo-theme-material))
> GNU GENERAL PUBLIC LICENSE
> Version 3, 29 June 2007
>Copyright (C) 2007 Free Software Foundation, Inc. <http://fsf.org/> Everyone is permitted to copy and distribute
 >verbatim copies of this license document, but changing it is not allowed. 
