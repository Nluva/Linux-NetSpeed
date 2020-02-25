在之前的文章里我说过：**对于出口带宽，我们常常采用BBR，锐速等TCP加速软件来争夺带宽提高自己的速度。**

但是原版的BBR并没有太多**侵略性**，在这个人人都用TCP加速的大环境下，BBR的加速功效就略显不足了。loc的大佬专门改进了下这个BBR，使BBR具有了侵略性。

最近我也连续购买了几个服务器，每次都手动搭建，感觉到十分麻烦，干脆写个脚本吧。由于是第一次接触shell脚本这一方面的内容，写起来感觉十分吃力，且与一般的高级语言语法~~差别有些大~~。所有有些不足的地方欢迎在下方评论反馈。

同时也加入了**锐速一键换内核，锐速一键安装，自动根据vps情况优化锐速参数，一键优化内核参数。**

也可以在锐速，BBR，BBR魔改版中自由切换。

## 一键脚本

![Linux-NetSpeed](https://www.kie.cc/images/Linux-NetSpeed.png)


# Linux-NetSpeed
```
wget "https://github.com/ikym/Linux-NetSpeed/raw/master/tcp.sh" && chmod +x tcp.sh && ./tcp.sh
```

## 脚本说明

> 支持系统  
> Centos 6+ / Debian 7+ / Ubuntu 14+  
> BBR魔改版不支持Debian 8  

如果在删除内核环节出现这样一张图

![Linux-NetSpeed-1](https://www.kie.cc/images/Linux-NetSpeed-1.png)

**注意选择NO**

根据自己需求操作，重启后再使用`./tcp.sh`命令接着操作

脚本会自动检测安装的情况，请注意脚本菜单下的**状态检测**即可。

## 参考资料

 - 魔改BBR原帖：http://www.hostloc.com/thread-372277-1-2.html

 - 脚本参考：https://ylws.me/tech/68.html

 - 技术参考：http://51.ruyo.net/p/4415.html
 
 同时非常感谢vicer提供Lotserver一键脚本。
