title: ipv6校园网免流量
date: 2015-09-30 22:18:28
categories: 杂项
tags: [shadowsocks,ipv6]
---
我学校的校园网按10元6G收费，超出后3元1G，挺贵的。而ipv6的流量确实不计费的，国内的教育网都有ipv6，可以用来免费上网。效果肯定不如收费模式，但是还算比较稳定。
## 基本思路
基本思路就是利用在服务器上搭建shadowsocks，本地填入服务器的ipv6地址，从而使得上网的流量全部走ipv6，来免流量上网。而国内的VPS基本没有ipv6，所以只能拿境外的服务器做代理，顺便有了一个*番羽墙*特效。
## 注册Digitalocean
对于学生来说，为了节省费用，建议先认证github education，可以得到digitalocean的100美金优惠券。digitalocean最便宜的是5美元的一个月，自己只要花5美元就能激活账户，加上github送的100美金，差不多可以用两年。进入我的[推广链接注册](www.digitalocean.com/?refcode=c7f58a8dc827)的话，可以多获得10美元的优惠券。

认证github education的方法请参考[学生免费享受 GitHub 提供的开发包](http://www.caoqq.net/github-pack.html)。
## 安装shadowsocks
目前Shadowsocks服务器端拥有四种语言版本，分别是：

- Shadowsocks-Python
- Shadowsocks-libev
- Shadowsocks-Go
- Shadowsocks-NodeJS

我装的是Shadowsocks-Python。
Linux发行版本，我选择的是Debian 7的32位版本。之所以选择这个是为了装后面的优化工具锐速。
digitalocean建立Droplets的过程可以参考这个[清北校园网如何配置免流量ipv6环境?](http://www.zhihu.com/question/25261199)

以下操作假定已经取得root权限下操作完成。


```
apt-get update  #更新软件源
apt-get install python-pip  #安装pip包管理器
pip install shadowsocks
apt-get install python-m2crypto     #安装加密库
```
## 配置Shadowsocks
```
apt-get install vim     #安装vim
vim /etc/shadowsocks.json #编辑配置文件
```
```
{
    "server":"::", 
    "server_port":8388,
    "local_address": "127.0.0.1",
    "local_port":1080,
    "password":"mypassword",
    "timeout":300,
    "method":"aes-256-cfb",
    "fast_open": false
}
```
| 字段 | 含义 |
|------|------|
|server|填写你的服务器ip地址|
|server_port	|填写服务器的端口号|
|local_port|	填写本地监听地址，一般为127.0.0.1|
|local_port	|填写本地端口号（一般为1080）|
|password	|填写你的Shadowsocks密码|
|timeout	|超时时间，单位为秒|
|method	|加密方式，推荐使用rc4-md5加密|
|fast_open	|打开或者关闭TCP TASTOPEN|

## 其他完善
更多完善请参考[Digitalocean配置shadowsocks服务器、优化笔记](http://notes.xiamo.tk/2015-06-17-Digitalocean%E9%85%8D%E7%BD%AEshadowsocks%E6%9C%8D%E5%8A%A1%E5%99%A8-%E4%BC%98%E5%8C%96%E7%AC%94%E8%AE%B0.html)
## 试用账号及使用方法
```
ip地址： 2605:f700:40:c00::bc0c:a251
端口  11810 
密码 bTQ7qoD5 
加密方式：aes-256-cfb
```
使用方法可以参考我前面的博客[科学上网新方法（附帐号）](http://linjiangxian998.com/2014/11/29/six/)

## 傻瓜式方法
上面的方法就是手工搭建免流量上网的过程，如果你还是觉得太麻烦，其实有一个偷懒的办法。就是直接买可以提供ipv6的shadowsocks账号。省去了搭建和优化的麻烦。我简单在谷歌上搜索了一下，找了个四个看起来满足条件，价格又不算贵的ss服务商。

[枫叶主机](http://www.fyzhuji.com/aff.php?aff=1438)

[ShadowSU](http://www.shadowsu.com/shadowsocks.html)

[SSX Shadowsocks](https://www.youss.org/)

[SHADOWSS](http://www.shadowss.net/)

其中我买过枫叶主机的shadowsocks，我买的是中级套餐，当时是80元一年，一个月60G，有ipv6节点。现在涨价了变成了120一年。其他三家我也没买过，仅供参考。