---
layout: post
title: 用Github和jekyll搭建个人博客（Win10版）
category: 工具
tags: Jekyll
keywords: Jekyll,Github
description: 
---
## 用Github和jekyll搭建个人博客（Win10版） ##
Mac比较方便，Windows也能用。
###一、注册Github、创建repository###
1. 注册GitHub账号，例如账户名为abc。
2. 创建一个与账户名对应的repository，例如abc.github.io。
3. 复制该repository的地址至剪贴板，例如https://github.com/abc/abc.github.io.git。

###二、安装jekyll###
 进入[jekyll中文官网](http://jekyll.com.cn/docs/installation/)，按照指导安装jekyll。这个过程可能有点麻烦，因为Windows下要先安装**ruby及其DEVELOPMENT KIT**。然后用其中包含的**gem**来安装jekyll。

###三、repository同步至本地###
1. 安装本地[GitHub Desktop](https://desktop.github.com/)
2. Windows菜单处启动git-bash,github上的工程复制到本地文件目录。
	
		git clone https://github.com/abc/abc.github.io.git
之后，GitHub安装目录下就会多出一个文件夹——*abc.github.io.git*。即Github官网上的repository已同步至本地文件夹。
###四、下载blog模板，用jekyll本地预览。###
1. 下载一个blog[模板](http://jekyllthemes.org/)，所有文件解压到文件夹——*abc.github.io.git*。
2. 启动Windows的cmd，用jekyll预览blog。

		cd 	C:\Users\hello\abc.github.io #具体文件夹目录地址，请根据本机自行修改
		jekyll serve
1. 模板本身可能需要安装其他jekyll插件，看报错信息，见招拆招吧。不出意外的话，浏览器中输入**http://127.0.0.1:4000//**，即可本地预览blog了。

###五、推送blog模板至GitHub，生成blog的网址。###



- push推送比较简单，启动git-bash，输入代码如下。
	
	cd abc.github.io
	git add . #预备提交所有文件
	git commit -a -m "备注内容" #添加备注
	git push origin master #提交

提交后会提示输入GitHub的用户和密码。回到GitHub官网，刷新之前新建的repository,可以看到jekyll工程文件已经顺利提交到github上了。具体操作可参考[网络教程](http://jingyan.baidu.com/article/3ea51489d0dec852e61bba34.html)中的步骤4-12。

- 回到github中的工程界面，点击右上角的“Setting”选项，在GitHub Pages中可以看到个人博客的访问地址。

**GOOD LUCK :)**