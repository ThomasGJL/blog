---
title: golang轻量级框架 － Gin (一)
tags: golang gin
categories: golang
---

* TOC
{:toc}

Gin 是一个 Go (Golang) 语言框架。 它是一个拥有更好性能的 martini-like API 框架, 由于 httprouter，速度提高了近 40 倍。 如果你是性能和高效的追求者, 那么你会爱上 Gin。[在线文档]

一、安装和开始

安装比较简单，使用go get即可

	go get-u github.com/gin-gonic/gin
	
新建一个Go项目, 然后在项目根目录下新建一个main.go文件, 内容如下：

	package main
	
	import (
		"github.com/gin-gonic/gin"
	
		"net/http"
	)
	
	func main() {
	
		router := gin.Default()
	
		router.GET("/", func(c *gin.Context) {
			c.String(http.StatusOK, "Hello World")
		})
	
		router.Run(":8000")
	}
	
打开CMD窗口，进入项目目录， go run main.go, 如下图：

![golang-gin-1][golang-gin-1]

打开浏览器访问： http://127.0.0.1:8000/

![golang-gin-2][golang-gin-2]

二、用官方依赖mod创建项目

gomod全称go module（vgo）， 如同java maven的pom.xml文件，gomod依赖go.mod和go.sum文件来定义和管理依赖版本，文件通过go mod init 模块名命令生成，支持修改编辑

配置gomod，打开CMD窗口， 运行： 
	
	go env -w GO111MODULE=on
	
	go env -w GOPROXY=https://goproxy.io,direct
	
然后进入项目目录，运行： 

	go mod init your app name
	
会生成一个 go.mod 文件

运行： 

	go mod tidy
	
这个命令会手动维护项目的包依赖，会检测项目当前的依赖，做相应的记录或移除，也会生成一个go.sum 文件

	
三、热加载调试 Hot Reload

Gin 原生不支持，但有很多额外的库可以支持。例如

我采用的是： github.com/pilu/fresh

	go get -v -u github.com/pilu/fresh
	
启动项目换成 fresh 就可以了： 

	fresh run main.go	
	




[在线文档]: http://www.topgoer.com/gin%E6%A1%86%E6%9E%B6/

[golang-gin-1]: {{"/golang-gin-1.jpg" | prepend: site.imgrepo }}
[golang-gin-2]: {{"/golang-gin-2.jpg" | prepend: site.imgrepo }}

