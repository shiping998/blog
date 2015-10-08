title: 使用hexo建立个人博客（四）
date: 2014-11-24 21:41:52
categories: 建博客
tags: [hexo] 
---
**注**：对文本的操作推荐用[Sublime Text 2](http://www.sublimetext.com/2)、[notepad++](http://notepad-plus-plus.org/)、[EditPlus](https://www.editplus.com/download.html),不推荐用Word和Windows自带的记事本。Word保存的不是纯文本文件，而记事本会自作聪明地在文件开始的地方加上几个特殊字符（UTF-8 BOM），结果会导致程序运行出现莫名其妙的错误。如果文本文件中有中文的话，保存为utf-8的编码，不会有乱码。
##部署博客到github上
用我推荐的文本编辑器打开_config.yml(如G:\hexo下)。你在部署时，要把下面的*shiping998*都换成你的账号名。
![Deployment](/img/5.JPG)
先右击空白处选择Git Bash执行
```
hexo g
```
使修改生效，再执行
```
hexo d
```
遇到![email](/img/6.JPG)输入你注册github时的用户名，然后回车
下面就是输入github的密码![password](/img/7.JPG) (*输入密码是不会显示，大胆的输就是了*)然后回车就提交成功了。你可以访问http://shiping998.github.io/  （shiping998换成你的用户名）查看你的博客。

每次提交都要输入账号密码，很麻烦。参看
[重复输入用户名密码的问题](http://zipperary.com/2013/05/26/ssh-errors-with-github/)可以解决这个问题。
##应用主题
博客虽然建成了但是默认主题不好看，hexo提供了一些主题（相当于皮肤）使我们的博客看起来更高大上一些。例如我用的就是Pacman主题。大家可以在[这里](https://github.com/hexojs/hexo/wiki/Themes)看到hexo的各种主题。我比较推荐我用的Pacman主题或者是和它类似的Jacman主题。下面我以Pacman为例简要介绍一下如何安装和使用。
###安装
在Git Bash中输入
```
$ git clone https://github.com/A-limon/pacman.git themes/pacman
```
###启用
修改你的博客根目录（hexo)下的_config.yml配置文件中的theme属性，将其设置为pacman。
![theme](/img/8.JPG)
更多配置可以参看[Pacman主题介绍](http://yangjian.me/workspace/introducing-pacman-theme/)
***
如果你想使用Jacman主题，看以参看[如何使用 Jacman 主题](http://wuchong.me/blog/2014/11/20/how-to-use-jacman/)
##写博客
前面费了不少劲搭建博客，最终目的还是为了写博客。你可能会说就是直接写呗。但是hexo是使用markdown语法写博客的。不过不要担心，markdown 并不困难，它其实就是用一些符号来控制文本格式，和自然书写区别不大。下面我就讲一下如何写博客。
在Git Bash输入
```
hexo new "my new post"
```
（my new post是标题，可以自己定义）就在hexo\source\_posts中新建了一个my-new-post.md的文件，用我之前说的文本编辑器打开它，对它进行编辑就可以了。保存后，再依次执行
```
hexo g
hexo d
```
博客就有了一篇文章。
书写时要按照markdown的格式，可以使用在线的[markdown编辑器](https://www.zybuluo.com)进行编辑然后复制过去。语法很简单，可以看一下[献给写作者的 Markdown 新手指南](http://www.jianshu.com/p/q81RER)这篇教程。这篇教程本身就是在[简书](http://www.jianshu.com)上用markdown写成的，你也可以使用简书书写。
我再附上一张简明的图，使大家上手更快些。![markdown](/img/9.JPG)
***
事实上如果你不想花钱，到这里就已经完成了博客的搭建。我的教程还有很多疏漏，更详细的教程可以参看[hexo系列教程](http://zipperary.com/categories/hexo/)。
***
下一篇我将讲一下购买域名和绑定域名的问题。
