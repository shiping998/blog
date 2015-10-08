title: 科学上网新方法（附帐号）
date: 2014-11-29 11:03:34
categories: 杂项
tags: [shadowsocks] 
---
科学上网就是访问国内网络无法访问的网站，比如facebook等。我以前用过goagent，最近shadowsocks比较流行。shadowsocks实质上也是一种socks5代理服务，shadowsocks仅针对浏览器代理，不能代理应用软件，比如youtube、twitter客户端软件。
1.如果是windows平台，可以从[百度网盘](http://pan.baidu.com/s/1bn3WQpp)下载。
2.运行解压后文件夹中的“shadowsocks.exe”，按照我给的账号设置好shadowsocks的账号信息，点save。
```
ip地址： 2605:f700:40:c00::bc0c:a251
端口  11810  
密码 bTQ7qoD5 
加密方式：aes-256-cfb
```
该账号到期时间是12月11日
3.使用可以安装插件的浏览器，比如chrome、火狐、360浏览器、搜狗浏览器之类的，在扩展里面找到Proxy SwitchySharp插件（找不到可以从[百度网盘](http://pan.baidu.com/s/1bnrP9iZ)下载，把下载的crx文件拖进浏览器去即可安装）

**现在这个插件的作者开发了新的插件SwitchyOmega，推荐使用这个，设置和SwitchySharp类似。**

4.设置Proxy SwitchySharp
右键点击浏览器右上角的地球图标，『选项』-『情景模式』-『新建情景模式』，按如下图设置![](/img/19.png)
然后进入『切换规则』，三个框全勾选，『在线规则列表』中填写
```
https://autoproxy-gfwlist.googlecode.com/svn/trunk/gfwlist.txt
```
保存，立即更新列表。
![](http://ww2.sinaimg.cn/large/5e8cb366jw1eixhdqrfaxj20ot04i74s.jpg)
平时Proxy SwitchySharp保持这种状态就可以。
![](/img/18.jpg)
注意如果要科学上网的话，shadowsocks软件要开着，且账号可用才可以。
shadowsocks在linux mac 安卓 ios平台都有客户端，都可以使用。
***
另外推荐一个代替谷歌的网站[谷粉搜搜](http://gufensoso.com/),搜索结果结果由香港谷歌实时提供 ，但是速度比直接访问谷歌快很多。我真心体会到谷歌在搜索技术内容时，比百度准确很多。
