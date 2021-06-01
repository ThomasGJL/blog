---
layout: post
title: 'pyspark设置python的版本'
category: spark
tags: spark
keywords: pyspark python
excerpt: "PySpark 在工作程序中都需要使用的为默认环境的python版本，怎样把python的版本切换成3的版本，您可以通过 `PYSPARK_PYTHON` 指定要使用的Python版本。"
---

## 目录

### 说明

PySpark 在工作程序中都需要使用的为默认环境的python版本，怎样把python的版本切换成3的版本，您可以通过 `PYSPARK_PYTHON` 指定要使用的Python版本。

### 处理步骤

#### 1.python3 环境需要提前安装好，如果没按照可以参考[centos7 下python2与python3共存](https://www.studytime.xin/python/2020/01/20/python-centos7-install.html)

#### 2.修改spark-env.sh文件, 在末尾添加`export PYSPARK_PYTHON=/usr/bin/python3`

#### 3.若为集群环境，需要把修改后的 spark-env.sh 分发到其他子节点的spark安装包下的conf目录下

#### 4.修改spark安装包bin目录下的pyspark，修改下图红色方框的位置，将原来PYSPARK_PYTHON=python改成PYSPARK_PYTHON=python3，同样的，其他子节点也都需要修改

![修改前](https://static.studytime.xin/image/articles/20200308153043.png)

```
if [[ -z "$PYSPARK_PYTHON" ]]; then
  if [[ $PYSPARK_DRIVER_PYTHON == *ipython* && ! $WORKS_WITH_IPYTHON ]]; then
    echo "IPython requires Python 2.7+; please install python2.7 or set PYSPARK_PYTHON" 1>&2
    exit 1
  else
    PYSPARK_PYTHON=python3
  fi
fi
```
#### 5.重启Spark，启动pyspark,可发现python的版本已切换成3.6.4的版本