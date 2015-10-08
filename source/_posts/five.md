title: 使用hexo建立个人博客（五）购买域名、设置DNS
date: 2014-11-28 11:06:07
categories: 建博客
tags: [hexo] 
---
有了域名，再加上一些优化，就可以在搜索引擎里搜到你的博客了。域名我是在Goddady里买的，我在前面已经讲过了为什么我在这里买，所以教程以Goddady为例。Goddady支持支付宝，支付比较方便。我的域名一年58元。我现在觉得我选的这个域名不太好，太长了。不过不用担心，域名是自己起名的，你可以设一个自己认为好的域名，只要它没被注册。
##购买域名
首先进入[Goddady](https://www.godaddy.com/)官网，网站是英文的，不过比较容易懂。如果把English旁边的按钮选成CNY，就是按人民币算的钱。没有账号点击Register注册-Creat My Accout。
![注册](/img/10.JPG)
###1、查你想要的域名
![](http://pic.yupoo.com/vankos_v/DKfZ9NWd/jD41I.png)
###2、查到适合的域名之后选择「continue to Cart」
![](/img/11.JPG)
###3、godaddy附加收费服务，不要管，继续「continue to Cart」
![](/img/12.JPG)
![](/img/13.JPG)
###4、确认购买。修改购买年限，默认是两年，可以修改成1/2/3/5/10年，随自己喜欢。我买的一年。
![](/img/14.JPG)
可以上网搜godaddy的优惠码，找一个填进这里，填完之后，会便宜一些
![](/img/15.JPG)
###5、结算。登录或注册界面，填完必要的信息之后，选择用支付宝结算。
![](http://pic.yupoo.com/vankos_v/DKg3N752/5hiii.png)
###6、检查。结算后，重新登录，去「My Account」，域名已经显示在你的账户了。
![](/img/16.JPG)
###7、补充一些注意事项：

输入优惠码没有优惠或者优惠幅度较低，请清除浏览器cookies再尝试；
如果没有支付宝支付选项，有可能是使用的优惠码不支持支付宝，请重新清除浏览器cookies再尝试；
注册时用户填写信息时一定要输入正确的邮箱名字，否则修改十分麻烦。
买完域名之后一定要记得去自己的邮箱查看激活邮件，否则域名激活不了
##域名绑定
###1.CNAME设置
在hexo\source下新建一个名字为CNAME文件（没有扩展名），打开它在里面输入你购买的域名，保存。
###2.DNS设置
推荐使用DNSpod，快，免费，稳定，中文。
首先注册[dnspod](https://www.dnspod.cn/),添加域名，进行如下设置
![](/img/17.JPG)
其中A的两条记录指向的ip地址是github Pages的提供的ip

192.30.252.153
192.30.252.154
最后一个CNAME要填 你的github用户名.github.io（就是你创建的那个 repository的名字，比如我的就是shiping998.github.io）
###3.去Godaddy修改DNS地址
更改godaddy的Nameservers为DNSpod的NameServers。
####1、点击「My Account」，管理我的域名。
![](http://pic.yupoo.com/vankos_v/DKguRB1h/dqHAZ.jpg)
####2、点击域名。
![](http://pic.yupoo.com/vankos_v/DKguScNK/UWvp.jpg)
####3、将godaddy的Nameservers更改成f1g1ns1.dnspod.net和f1g1ns2.dnspod.net 
![](http://pic.yupoo.com/vankos_v/DKguQvcp/3dN7k.jpg)
![](http://pic.yupoo.com/vankos_v/DKijvnQy/JOE82.png)
***
稍等一会，输入域名就可以访问你的博客了。这篇教程参考了很多[如何搭建一个独立博客——简明Github Pages与Hexo教程](http://blog.sina.com.cn/s/blog_617ccc0c0101h84p.html)，在此表示感谢。
至此，搭建hexo博客的系列教程全部结束了，还有很多问题我可能没提到，自己可能也不清楚。那就只能大家自己搜索了。看起来教程比较繁琐，但如果搭建成功，回过头来想想，也没有那么复杂，还有一定成就感。希望你能拥有自己的博客。