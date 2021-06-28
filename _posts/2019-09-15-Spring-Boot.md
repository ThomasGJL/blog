---
title: SpringBoot项目创建方式一：Spring Initializr
tags: java spring SpringBoot
categories: java
---

* TOC
{:toc}

使用 Spring Initializr 初始化 Spring Boot 项目
Spring Initializr 从本质上说就是一个Web应用程序，它能为你构建Spring Boot项目结构。虽然不能生成应用程序代码，但它能为你提供一个基本的项目结构，以及一个用于构件代码的Maven或者Gradle构建说明文件。
Spring Initializr 有几种用法：

    通过Web界面使用
    通过Spring Tool Suite使用
    通过IntelliJ IDEA使用
    通过Spring Boot CLI使用

使用Web方式：
要使用Spring Initializr，最直接的办法就是使用浏览器打开[https://start.spring.io]，应该能看到一个类似于下图的一个表单。

![Spring-Boot-1][Spring-Boot-1]

	Project: 选择是使用Maven还是Gradle来创建项目
	Language: 选择使用的开发语言
	Spring Boot: 选择Spring Boot版本
	Project Metadata: 项目的一些基本信息
	
	Dependencies: 选择需要的依赖

![Spring-Boot-2][Spring-Boot-2]

填好表单，选好依赖后，可以点击下方GENERATE，导出下载项目

[https://start.spring.io]: https://start.spring.io


[Spring-Boot-1]: {{"/Spring-Boot-1.jpg" | prepend: site.imgrepo }}
[Spring-Boot-2]: {{"/Spring-Boot-2.jpg" | prepend: site.imgrepo }}


