---
layout: post
title:  "Come to jekyll!"
date:   2013-12-14 00:57:57
---

很久没有写些自己的东西，工作已经两年多了，项目上陆陆续续地做着，工作欲望的确没有以前强了，需要好好整理和面对。

今天写写，终于在mac上搭好了jekyll blog，

sudo gem install jekyll
(if the process is so slow， you should replace the gem sources)
gem sources -remove your-origial-resource-url
get sources -a http://ruby.taobao.org/

jekyll // test the installation is done
jekyll new yourblogfolder

jekyll serve --watch

git add -i
git config --global user.name "nevermosby"
git config --global user.email robolwq@qq.com
git commit -m "first comit for my new blog"
git remote add newblog https://github.com/nevermosby/nevermosby.github.io.git
git push newblog master

Check out the [Jekyll docs][jekyll] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll's GitHub repo][jekyll-gh].

[jekyll-gh]: https://github.com/mojombo/jekyll
[jekyll]:    http://jekyllrb.com
