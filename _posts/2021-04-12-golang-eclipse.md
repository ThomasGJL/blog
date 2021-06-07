---
title: Eclipse Golang 开发环境搭建
tags: golang eclipse GoClipse
categories: golang
---

* TOC
{:toc}

Go是从2007年末由Robert Griesemer, Rob Pike, Ken Thompson主持开发，后来还加入了Ian Lance Taylor, Russ Cox等人，并最终于2009年11月开源，在2012年早些时候发布了Go 1稳定版本。现在Go的开发已经是完全开放的，并且拥有一个活跃的社区。 引用自[菜鸟教程]

安装包[下载地址]

以下是我总结的安装步骤：

1、下载安装包后，直接双击安装即可， 注意： 选择安装目录不能有空格。 推荐C:\Go

2、环境变量设置

GOROOT 你的安装路径， 我的是C:\Go

GOBIN %GOROOT%\bin

GOPATH 是一些用于 go 来查找包的目录列表，使用 import "包名" 的时候，如果在 GOROOT 中找不到，应该会转向到 GOPATH 中寻找。注意： 不能将 GOPATH 和 GOROOT 设置成一样的

为了方便调试可以把GOBIN添加到Path中

3、测试安装结果 go env, 这个命令可以列出你本地的环境信息， 如下图：

![golang-eclipse-1][golang-eclipse-1]

4、打开你的Eclipse， Help->Eclipse Marketplacke，输入GoClipse, 选择安装即可

![golang-eclipse-2][golang-eclipse-2]

5、安装完成后重启 Eclipse，进行进一步的配置， Windows->Preferences->Go，配置Go安装目录和GoPath, 保持和环境变量一直就可以

![golang-eclipse-3][golang-eclipse-3]

6、配置 Go IDE 开发的三个工具：gocode  guru  godef 并选择 gofmt位置， 我通过Download直接下载，但是网上有些教程说guru不能直接下载，所以这里列出获得guru.exe生成步骤

6.1、从 github 上下载 guru 的源码 [https://github.com/golang/tools]，解压缩后改名为 tools

6.2、在 %GOPATH%\src 路径下新建路径 golang.org\x

6.3、将 tools 文件夹移动到 %GOPATH%\src\golang.org\x 路径下

6.4、打开 cmd，切换路径到 %GOPATH%\bin 下，然后执行 go build golang.org\x\tools\cmd\guru，执行完后，会在 %GOPATH%\bin 下生成 guru.exe 文件

![golang-eclipse-4][golang-eclipse-4]

7、新建一个Go项目，写个简单例子测试

![golang-eclipse-5][golang-eclipse-5]

![golang-eclipse-6][golang-eclipse-6]


[菜鸟教程]: https://www.runoob.com/go/go-tutorial.html
[下载地址]: https://golang.google.cn/dl/
[https://github.com/golang/tools]: https://github.com/golang/tools

[golang-eclipse-1]: {{"/golang-eclipse-1.jpg" | prepend: site.imgrepo }}
[golang-eclipse-2]: {{"/golang-eclipse-2.jpg" | prepend: site.imgrepo }}
[golang-eclipse-3]: {{"/golang-eclipse-3.jpg" | prepend: site.imgrepo }}
[golang-eclipse-4]: {{"/golang-eclipse-4.jpg" | prepend: site.imgrepo }}
[golang-eclipse-5]: {{"/golang-eclipse-5.jpg" | prepend: site.imgrepo }}
[golang-eclipse-6]: {{"/golang-eclipse-6.jpg" | prepend: site.imgrepo }}


