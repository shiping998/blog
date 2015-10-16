title: 使用hexo建立个人博客（三）hexo配置
date: 2014-11-16 21:52:25
categories: 建博客
tags: [hexo] 
---
## 安装Node.js
hexo是一款基于Node.js的博客框架，所以要先安装Node.js环境。在 Windows 下安装 Node.js 只需要在[Node.js](http://nodejs.org/)官网，点击install便可以下载安装程序。下载之后直接安装就可以了。安装完之后请重启电脑一次。
## 安装mygit
我们将在这个软件输入一些命令进行操作。从http://msysgit.github.io 下载，然后按默认选项安装即可。

安装完成后，在空白处右击鼠标选择Git Bash蹦出一个类似命令行窗口的东西，就说明Git安装成功！
![Git Bash](/img/4.jpg)
在Git Bash输入
```
git config --global user.name "Your Name"
git config --global user.email "email@example.com"
```
Your Name要填你在github中注册的用户名，email@example.com填你注册github时用的邮箱。
## 安装hexo
在任意空白处右击鼠标选择Git Bash,输入
```
npm install -g hexo@2.8.3

```
## 创建hexo文件夹
在你喜爱的文件夹下（如G:\hexo），在G:\hexo（你自己的文件可能跟我不一样）内点击鼠标右键，选择Git bash，执行以下指令。Hexo会自动在目标文件夹建立网站所需要的所有文件。
```
hexo init
```
## 安装依赖包
```
npm install

```
## 本地网站
执行以下命令(如G:\hexo)
```
hexo g
hexo s
```
g即是generate，可以写整个单词generate，也可以只写g。s也是同理，即是server。
以上两步就建起了本地博客，按照提示可以在浏览器中输入http://localhost:4000 查看。但是博客还没有放到github上，别人看不到。下一篇我讲一下怎么把博客托管到github上，这样就是真正的博客了。