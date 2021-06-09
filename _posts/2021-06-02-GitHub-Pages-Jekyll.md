---
title: GitHub Pages + Jekyll 快速搭建个人博客
tags: GitHub Jekyll Blog
categories: Jekyll
---

* TOC
{:toc}

本文主要讲如何使用 Jekyll 在 Github 搭建博客(GitHub Pages + Jekyll )，搭建博客还有其它的方法，在这之前我没在 github 上搭建博客，到成功的在github建立了博客，博客地址请点击[这里][这里]浏览 ，搭建一个博客需要的技术很少，直接Clone一个主题，然后修改个人信息，放入自己的博客就好。

我使用的是 [jekyll主题][jekyll主题]， 不了解 jekyll 的小伙伴请[点击这里][点击这里]。 可以先去下载自己喜欢的主题，然后上传到github

步骤如下:

第一大步：注册github并创建一个仓库

1.用自己的邮箱注册

![github1][github1]

2.新建一个仓库

登录之后，点击右边New按钮

![github2][github2]

然后出现下面的内容

![github3][github3]

第一个是要创建的仓库的名称。名称不能乱取，需要写成：用户名.github.io。假如我用户名是thomasgjl，那么这里仓库名就需要填入thomasgjl.github.io。

第二个表示是否需要创建一个README文件，个人认为可要可不要，因为找的主题模板里面有。

创建之后

![github4][github4]

这里显示的url，即当前仓库的远程地址，可用于clone或者push。


第二大步：安装jekyll

1.下载并安装git

2.安装ruby

这是下载链接：[https://rubyinstaller.org/downloads/][https://rubyinstaller.org/downloads/]

由于需要安装ruby和devkit，我就下载了官方推荐的两个合成一个的安装包，如图：

![github5][github5]

安装完之后，会自动勾选，点击finish就行，然后会自动弹出dos窗口，然后让你选择

![github6][github6]

我选择的1，第二个选项应该是一样的效果吧。。。

到最后会提醒你安装成功了，然后点击enter就行了。

3.安装jekyll.

打开dos，输入gem install jekyll，开始安装jekyll。

安装完jekyll之后，在dos里面输入jekyll -v，如果出现版本号，则说明jekyll安装成功。如图：

![github7][github7]

4.找自己喜欢的主题

jekyll主题模板下载： [http://jekyllthemes.org][http://jekyllthemes.org]

这是一部分主题，选一个自己喜欢的主题。比如选择第一个，进入。这个时候你就有三个选择 

a) 如果选择homepage，你就进入到该主题的GitHub主页，然后该页面有个clone绿色的按钮，有个url地址，这个地址就能用来克隆该主题的所有文件 
b) download就不用说了。直接解压到所需文件夹里就行 
c) 选Fork

5.安装bundle

在dos里面，输入gem install bundler

![github8][github8]

出现这个就算安装好了。


6.修改配置文件

在clone或者下载之后，各种需要的文件都安装完成之后。修改_config.yml中的配置

url: "http://127.0.0.1:4000"

imgrepo: "http://127.0.0.1:4000/static/img"

7.本地预览

配置完成后，在cmd窗口项目当前目录下，输入bundle exec jekyll s  这里s是serve的简写。 然后就可以在 localhost:4000/

![github9][github9]
![github10][github10]

8.本地文件push到github指定仓库中

修改_config.yml的配置

url: "https://yoursitename"

imgrepo: "https://yoursitename/static/img"



[这里]: https://thomasgjl.github.io/blog
[jekyll主题]: http://jekyllthemes.org/
[点击这里]: https://jekyllrb.com/
[https://rubyinstaller.org/downloads/]: https://rubyinstaller.org/downloads/
[http://jekyllthemes.org]: http://jekyllthemes.org

[github1]: {{"/github-pages-Jekyll-1.png" | prepend: site.imgrepo }}
[github2]: {{"/github-pages-Jekyll-2.jpg" | prepend: site.imgrepo }}
[github3]: {{"/github-pages-Jekyll-3.jpg" | prepend: site.imgrepo }}
[github4]: {{"/github-pages-Jekyll-4.jpg" | prepend: site.imgrepo }}
[github5]: {{"/github-pages-Jekyll-5.jpg" | prepend: site.imgrepo }}
[github6]: {{"/github-pages-Jekyll-6.png" | prepend: site.imgrepo }}
[github7]: {{"/github-pages-Jekyll-7.jpg" | prepend: site.imgrepo }}
[github8]: {{"/github-pages-Jekyll-8.png" | prepend: site.imgrepo }}
[github9]: {{"/github-pages-Jekyll-9.jpg" | prepend: site.imgrepo }}
[github10]: {{"/github-pages-Jekyll-10.jpg" | prepend: site.imgrepo }}
