---
title: composer 安装 laravel
tags: PHP Composer Laravel
categories: PHP
---

* TOC
{:toc}

Composer是php的依赖管理工具，不是包管理器。 

安装方式：

（1）Composer-Setup.exe 

 　　Win操作系统、需FQ

（2）composer.phar

　　通用安装方式、不需要FQ，win和linux都可以

 

直接下载：

[https://getcomposer.org/download/]

命令行下载:

php -r "readfile('https://getcomposer.org/installer');" | php


局部安装

将composer.phar文件复制到任意目录，然后通过php composer.phar指令即可使用composer了。

全局安装

max或者linux系统

sudo mv composer.phar /usr/local/bin/composer

win系统

将composer.phar拷贝到php.exe同级目录

新建composer.bat文件，并将下面的代码保存到该文件中

@php "%~dp0composer.phar" %*

#注意： 把 PHP的目录加到Path里就可以在CMD窗口的任何目录使用composer命令 

Composer中国全量镜像所做的就是缓存所有安装包和元数据到国内的机房并通过国内的CDN进行加速，这样

就不必再去国外的网站发起请求了，更加快速方便。

查看当前的镜像地址

composer config -g repo.packagist

 
查看包信息

composer search laravel

验证composer安装，CMD窗口输入composer


![php-composer-laravel-1][php-composer-laravel-1]


使用 composer 安装 laravel


composer create-project laravel/laravel your-project-name ----prefer-dist "5.1.*" 


[https://getcomposer.org/download/]: https://getcomposer.org/download/


[php-composer-laravel-1]: {{"/php-composer-laravel-1.jpg" | prepend: site.imgrepo }}




