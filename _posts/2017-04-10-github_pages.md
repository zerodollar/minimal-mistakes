---
comments: true
title: "github上的静态博客方法"
header:
  teaser: /assets/images/teaser.jpg
categories:
  - github
tags:
  - github博客
  - jekyll
---
# 安装
教程较多，在github上搜索github pages，[minimal-mistakes](https://mmistakes.github.io/minimal-mistakes/)不错,fork这个仓库，重命名为zerodollar.github.io,clone到本地(以下都以zerodollar为github的用户名)
```
git clone https://github.com/zerodollar/zerodollar.github.io.git --depth=1
git clone git@github.com:zerodollar/zerodollar.github.io.git --depth=1
```

# 本地调试方法
基于[jekyll](http://jekyllrb.com/)，该工具本地使用方法：
```
cd zerodollar.github.io.git
gem install jekyll bundler
bundle install
bundle exec jekyll serve    
```
# 配置
*  _data/navigation.yml
每一个title是一个目录
* _data/ui-text.yml
多语言支持，默认不用修改
* _config.yml 
```
url                      : "https://zerodollar.github.io"
repository               : "zerodollar/blog"

```

