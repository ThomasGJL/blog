---
title: Wagtail — 基于Django的Python CMS
tags: python django wagtail
categories: python
---

* TOC
{:toc}

Django 是一个开放源代码的 Web 应用框架，由 Python 写成。Django 遵守 BSD 版权，初次发布于 2005 年 7 月, 并于 2008 年 9 月发布了第一个正式版本 1.0 。Django 采用了 MVT 的软件设计模式，即模型（Model），视图（View）和模板（Template）。 引用自[菜鸟教程]。 Django的英文[官方文档]。

[https://github.com/wsvincent/awesome-django]

wagtail 是一个用Python编写的开源CMS，并构建在Django框架上。 wagtial的英文官方[文档]

[https://github.com/springload/awesome-wagtail]

wagtail基本使用命令：

安装： pip install wagtail

初始化： wagtail start mysite

创建超级管理员： python manage.py createsuperuser

模型更改： python manage.py makemigrations和python manage.py migrate， 这两条命令可以合并成一条 python manage.py makemigrations && python manage.py migrate

新建模块： python manage.py startapp newpage

启动项目： python manage.py runserver 

静态文件收集： python manage.py collectstatic

导出数据： python manage.py loaddata

导入数据： python manage.py dumpdata


[https://github.com/wsvincent/awesome-django]: https://github.com/wsvincent/awesome-django
[https://github.com/springload/awesome-wagtail]: https://github.com/springload/awesome-wagtail

[菜鸟教程]: https://www.runoob.com/django/django-tutorial.html
[官方文档]: https://django.readthedocs.io/en/stable/
[文档]: https://docs.wagtail.io/en/stable/