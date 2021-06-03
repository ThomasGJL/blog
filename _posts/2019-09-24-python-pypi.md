---
title: python封装自定义包上传到Pypi
tags: python pypi Github
categories: python
---

* TOC
{:toc}

什么是pypi?

简单的说pypi是一个python包的仓库，里面有很多别人写好的python库，你可以通过easy_install或者pip进行安装, 方便用户更方面的使用你的代码模块。 具体地址是：[https://pypi.org/][https://pypi.org/]

将代码打包并上传到pypi上，大体上分为以下几步：

1、首先创建一个项目，项目名字尽量明确定义包的用途， 项目的层级结构如下（完整的层级结构，dist是打包时候生成的，docs是文档目录，可以用来生成文档，这部分会放在[另一个博客]里）


![python-pypi-1][python-pypi-1]

1.1、创建setup.py文件，setup.py结构如下：

![python-pypi-2][python-pypi-2]

1.2、创建README.md文件，README.md是关于项目的描述文件，一般包含怎样安装项目，请参考我的自定义仓库的[说明文件]


1.3、创建业务逻辑文件代码，如下图

![python-pypi-3][python-pypi-3]


2、打包项目并上传


[https://pypi.org/]: https://pypi.org/
[另一个博客]: http://baidu.com
[说明文件]: https://github.com/ThomasGJL/django-github-storage/blob/main/README.md

[python-pypi-1]: {{"/python-pypi-1.jpg" | prepend: site.imgrepo }}
[python-pypi-2]: {{"/python-pypi-2.jpg" | prepend: site.imgrepo }}
[python-pypi-3]: {{"/python-pypi-3.jpg" | prepend: site.imgrepo }}
