---
title: windows下安装Apache2.4 + PHP7.2.16
tags: PHP Apache
categories: PHP
---

* TOC
{:toc}

一、安装apache2.4

1、下载apache，地址： [https://www.apachelounge.com/download/]

2、下载好之后，解压到自己想安装的目录，我是安装在C盘： C:\Apache24

用记事本打开C:\Apache24\conf\httpd.conf ，准备修改Apache配置文件。

搜索SRVROOT，在Define SRVROOT写上apache的安装目录, 如下图： 

![apache-php-1][apache-php-1]

3、配置完成之后，以管理员身份运行cmd窗口，输入httpd -k install -n apache2.4 命令安装apache， httpd.exe -k uninstall -n apache2.4卸载apache

4、启动apache

4.1、可以双击C:\Apache24\bin\ApacheMonitor.exe文件

4.2、也可以在cmd中以管理员身份输入httpd -n Apache2.4 -k start 启动apache

httpd -k start：不会提示详细的错误信息。  

httpd -n Apache2.4 -k start：会提示详细的错误信息，其中的"apache"修改为你的Apache服务名,可以到计算机服务里找。  

httpd -n Apache2.4 -k restart：重启。  

net start Apache2.4： 利用Windows托管服务命令。

4.3、打开计算机管理，找到apache服务项，选择后，右键单击，便可选择相应操作（启动、停止、重新启动） 

5、打开浏览器，输入： https://127.0.0.1/

![apache-php-2][apache-php-2]



二、安装PHP7.3.5

1、下载Thread Safe的PHP： [https://windows.php.net/download/]

下载之后解压到安装的目录下，我是安装在C盘: C:\Apache24\php

将php.ini-development复制重命名为php.ini

再打开apache下的conf中httpd.conf打开，在最后加上

	#php7 support
	LoadModule php7_module "C:/Apache24/php/php7apache2_4.dll"
	AddHandler application/x-httpd-php .php
	PHPIniDir "C:/Apache24/php/"
	AddType application/x-httpd-php .php .html .htm
	#configure the path to php.ini

2、再重启apache

3、验证PHP安装，新建index.php，内容： 
	
	<?php
	phpinfo()
	?>

打开浏览器，输入： https://127.0.0.1/index.php

![apache-php-3][apache-php-3]


三、给PHP安装SQL扩展

1、下载SQLSRV40.EXE（支持php7.0+），[https://www.microsoft.com/en-us/download/details.aspx?id=20098]

![apache-php-4][apache-php-5]

2、解压SQLSRV40.EXE文件

![apache-php-5][apache-php-5]

3、把php_pdo_sqlsrv_7_ts_x64.dll和php_sqlsrv_7_ts_x64.dll复制到php/ext目录下
注意：ts与nts的区别，看phpinfo


[https://www.apachelounge.com/download/]: https://www.apachelounge.com/download/
[https://windows.php.net/download/]: https://windows.php.net/download/
[https://www.microsoft.com/en-us/download/details.aspx?id=20098]: https://www.microsoft.com/en-us/download/details.aspx?id=20098


[apache-php-1]: {{"/apache-php-1.jpg" | prepend: site.imgrepo }}
[apache-php-2]: {{"/apache-php-2.jpg" | prepend: site.imgrepo }}
[apache-php-3]: {{"/apache-php-3.jpg" | prepend: site.imgrepo }}
[apache-php-4]: {{"/apache-php-4.png" | prepend: site.imgrepo }}
[apache-php-5]: {{"/apache-php-5.png" | prepend: site.imgrepo }}

