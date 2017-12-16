---
title: "github上的静态博客方法"
categories:
  - tools
tags:
  - github博客
  - jekyll
---
如何使用minimal-mistakes框架方便地在github上部署静态博客。


## 选型
- 手工搭建    
参考[github pages说明](https://pages.github.com)、[教程](https://help.github.com/categories/github-pages-basics/), 写html
- 使用博客框架
  - github  
    参考[自动页面生成器](http://blog.csdn.net/renfufei/article/details/37725057/) 
  - hexo  
     支持Markdown，使用Nodejs速度快，缺点：本地将markdown转换为html
  - jekyll  
    支持Markdown在线编辑，使用Ruby。bundle会监控文件修改自动更新。[这个教程](http://blog.csdn.net/on_1y/article/details/19259435#t8)不错
- 开发好的pages框架  
  jekyll系的[minimal-mistakes](https://mmistakes.github.io/minimal-mistakes), 

## 使用步骤
### 安装
将[minimal-mistakes](https://mmistakes.github.io/minimal-mistakes) fork到自己用户名zerodollar.github.io， git clone 到本地，进入本地目录
```
cd zerodollar.github.io
sudo gem install jekyll bundler
bundle install
bundle exec jekyll serve
```
公网访问[https://zerodollar.github.io](https://zerodollar.github.io)，本地访问[http://127.0.0.1:4000](http://127.0.0.1:4000)  
安装gem组件时，有错误查看对应组件帮助，比如[nokogiri](http://www.nokogiri.org/tutorials/installing_nokogiri.html)编译失败
```
brew install libxml2
bundle config build.nokogiri --use-system-libraries   --with-xml2-include=$(brew --prefix libxml2)/include/libxml2
bundle install
```
目录结构参考[Structure](https://mmistakes.github.io/minimal-mistakes/docs/structure/)
### 配置minimal-mistakes
参考[配置](https://mmistakes.github.io/minimal-mistakes/docs/configuration/)

- 定制私有信息  
locale 语言、title  主题、name、description、author信息等
- 打开搜索  
```
search: true
```
- 导航
修改navigation.yml， 注意url部分要在_config.yml的collections进行配置，否则访问时找不到url。
- 评论系统  
```
comments: true
```
业界老大disqus被墙，翻墙有教程。Disqus去[Disqus官方网站](https://disqus.com) 注册账号，在setting中选择add disqus to site，填写 Site URL，Site Name，Site Shortname。在<名字>.disqus.com中setting/advanced的Trusted Domains添加域名。
样例使用了staticman_v2，这是一个支持github和jekyll的非常好用的静态博客评论，评论和博客在一个站点上。  
staticman.yml中path修改成_data/comments目录下，并建立_data/comments目录
moderation: false 表示不需要审批自动提交
参考[STATICMAN指导](https://staticman.net/docs/index.html)
  - 仓库
  博客项目Settings/Collaborators添加staticmanapp，访问https://api.staticman.net/v2/connect/zerodollar/zerodollar.github.io/， 生效请求。

- RSS订阅
访问[](https://feedburner.google.com)Burn a feed right this instant
- 分享  
百度分享 ？
- 自动生成分类目录  
参考Breadcrumb
```
mv docs/_pages/  .
rm _pages/about.md
```
- 删除多余文件  
```
rm -fr .editorconfig .gitattributes .github 
rm -fr  ./docs ./test CHANGELOG.md 
rm -fr  README.md screenshot*png
```
- 升级  
```
git remote add upstream https://github.com/mmistakes/minimal-mistakes.git
git pull upstream master
```

## Jekyll原理
参考[Jekyll中国](http://jekyllcn.com/docs/structure/)，是将纯文本转换为静态博客网站，核心就是一个Ruby实现的文本转换引擎：任何标记语言（比如Markdown），Jekyll套入布局中，最终生成静态页面。


文件/ 目录 | 描述
------- | -------
_config.yml | [配置数据](http://jekyllcn.com/docs/configuration/)
_drafts|草稿，未发布的文章， --drafts选项支持预览
_includes|用于重用
_layouts|用于布局
_posts|文章YEAR-MONTH-DAY-title.md
_data|预置的网站数据
_site|转换好后的页面
.html<br>.markdown<br>.md<br>.textile|含义yaml头信息，都会被转换
其他文件|拷贝到_site中<br>assets中文件引用:`[下载 PDF]({{ site.url }}/assets/xxx.pdf)`


头信息：设置预定义、自定义的变量，在文档中用Liquid标签来访问这些变量

变量名称 | 描述
------- | -------
layout|使用_layouts下的对应模板文件
permalink|修改默认的URL：/year/month/day/title.html
published|不展示
xxx|自定义变量，模板通过{{ page.xxx }}引用
date|覆盖文件名中日期
category<br>categories|除了文件夹分类，指定其他的1~n个分类属性
tags|类似categories

excerpt_separator，文章第一次匹配前部分为摘要
集合Collections，除了文章特性，还有特有的属性和命名空间

