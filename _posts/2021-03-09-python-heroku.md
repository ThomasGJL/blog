---
title: Flask, Wagtail项目部署到Heroku平台
tags: python Flask Django Wagtail Heroku
categories: python
---

* TOC
{:toc}

Heroku是一个支持多种编程语言的云平台即服务。目前支持Ruby、Java、Node.js、Scala、Clojure、Python、PHP和Perl等语言，基础操作系统是Debian

一、配置Heroku

1、首先注册Heroku账号，点击通过[https://dashboard.heroku.com]注册一个账号，推荐gmail或hotmail

2、新建一个app
![python-heroku-1][python-heroku-1]

在deploy tab里会看到3种发布方式：

	1、Heroku Git Heroku CLI
	2、Github
	3、Container Registry Heroku CLI

个人推荐Github方式



![python-heroku-2][python-heroku-2]

3、在github.com新建一个Repositories，


4、选择Github，选择你的github下的Repositorie， 选择branch. 点击connect



[https://dashboard.heroku.com]: https://dashboard.heroku.com


[python-heroku-1]: {{"/python-heroku-1.jpg" | prepend: site.imgrepo }}
[python-heroku-2]: {{"/python-heroku-2.jpg" | prepend: site.imgrepo }}