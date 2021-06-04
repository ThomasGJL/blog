---
title: Readthedocs + Github + sphinx 创建在线文档
tags: python readthedocs Github
categories: Github
---

* TOC
{:toc}

在学习django、wagtail的时候，发现Readthedocs这样的文档结构很清晰，就想给自定义的库也创建一份这样的在线文档。 经过学习，总结了以下的步骤。

1、本地安装sphinx： pip install sphinx， pip install sphinx_rtd_theme，github上有很多开源的主题可以替换。

2、打开CMD窗口，进入文档目录（一般是docs），通过命令sphinx-quickstart快速配置， 生成目录结构如下图：

![readthedocs-sphinx-1][readthedocs-sphinx-1]

其中conf.py是配置文件，build文件是生成的html文件的位置

3、运行 make html命令，在build文件夹查看预览效果

4、上传代码至GitHub仓库, 然后去 [https://readthedocs.org/]注册账号,并关联GitHub仓库.

![readthedocs-sphinx-2][readthedocs-sphinx-2]

5、关联后导入你的项目，接着就可以build文档，bulid成功后，点击View Docs就打开就可以看到在线文档， 如下图： 

![readthedocs-sphinx-3][readthedocs-sphinx-3]


![readthedocs-sphinx-4][readthedocs-sphinx-4]

[https://readthedocs.org/]: https://readthedocs.org/

[readthedocs-sphinx-1]: {{"/readthedocs-sphinx-1.jpg" | prepend: site.imgrepo }}
[readthedocs-sphinx-2]: {{"/readthedocs-sphinx-2.jpg" | prepend: site.imgrepo }}
[readthedocs-sphinx-3]: {{"/readthedocs-sphinx-3.jpg" | prepend: site.imgrepo }}
[readthedocs-sphinx-4]: {{"/readthedocs-sphinx-4.jpg" | prepend: site.imgrepo }}
