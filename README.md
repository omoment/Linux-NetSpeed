# Linux-NetSpeed

在Chikage的脚本基础上加了bbrplus的内核切换与加速安装  

Chikage https://www.zhujidaba.com/470.html https://github.com/chiakge/Linux-NetSpeed

项目：https://github.com/cx9208/Linux-NetSpeed  
bbrplus介绍见：https://www.hostloc.com/thread-507165-1-1.html  

在vultr上Centos 7, Debian 8/9, Ubuntu 16/18测试通过,不支持ovz  
（bbrplus的debian/ubuntu内核已经弄好了，先加到这里了，我那个原来的项目还没加，毕竟这个很好用）  

![avatar](https://s1.ax1x.com/2018/12/24/F6XveP.png)

安装：
```
wget "https://github.com/chiakge/Linux-NetSpeed/raw/master/tcp.sh" && chmod +x tcp.sh && ./tcp.sh
```

提示证书错误的话
```
apt-get -y install ca-certificates
```
```
yum -y install ca-certificates
```

1. 先在[1 - 3]切换内核（第一次显示为bbr内核也要切换一遍），重启

出现这个选no
![avatar](https://s1.ax1x.com/2018/12/24/F6xwqI.png)

2. 重启后不用再下载脚本，直接 ./tcp.sh ，在[4 - 8]中选你要开的加速

"1. 安装 BBR/BBR魔改版内核"        对应4,5,6（原版，魔改，暴力魔改）  
"2. 安装 BBRplus版内核 "                对应7（plus）  
"3. 安装 Lotserver(锐速)内核"        对应8（锐速）  

3. 开启后再 ./tcp.sh  ， 显示开启成功则启动成功，你也可以自己手动确认  

现在你可以自由的切换你想要的加速，直到你不想折腾为止~  

https://www.hostloc.com/thread-508015-1-1.html
