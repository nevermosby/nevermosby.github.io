---
layout: post
title:  "Come to jekyll!"
date:   2013-12-14 00:57:57
---

很久没有写些自己的东西，工作已经两年多了，项目上陆陆续续地做着，工作欲望的确没有以前强了，需要好好整理和面对。

今天写写，终于在mac上搭好了jekyll blog，

通过gem获取jekyll模板（当然也可手动安装，此处不细说了）：

	sudo gem install jekyll

如果下载安装package的过程太长，你可能需要更换gem sources，调整cdn对你更快的那个
在中国大陆，一般可选择淘宝网提供的cdn：

	gem sources -remove your-origial-resource-url
	get sources -a http://ruby.taobao.org/

下载安装完成后，使用以下命令测试安装是否成功：

	jekyll

使用new命令来创建jekyll site：

	jekyll new yourblogfolder

开启jekyll server，并进行实时监听：

	jekyll serve --watch

建立起属于自己的jekyll blog，接下来要做的就是，将你的blog部署到大家可以看得到的地方。
这年头，程序员一般都会选择github作为展现自己的自媒体平台。这里简单介绍如何远程部署。
在这之前，你可能先要安装git，并且配置你的帐号信息

	git config --global user.name "nevermosby"
	git config --global user.email robolwq@qq.com

初始化你的想要作为repo的folder，在此目录下，使用以下命令：
	
	git init

使用交互式add file 命令，来标记你想添加到github的文件:
	
	git add -i

提交你的所做的所有修改:

	git commit -m "first comit for my new blog"

将当前的repo添加到远程的github服务器上，你需要指定这个repo（首次添加，为master分支）这个分支添加一个别名，
还有你已存在的github repo 地址，作为你local repo的远程映射目录：

	git remote add newblog https://github.com/nevermosby/nevermosby.github.io.git

最后通过push指令，部署到remote github repo上去，这里你需要指定刚才添加的别名，以及你想提交到remote repo上哪个分支：
	git push newblog master

这样，每次对local repo做啥修改，都可以通过 commit和push命令，重新部署github的repo。

