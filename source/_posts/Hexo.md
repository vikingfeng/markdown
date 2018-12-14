---
title: Hexo
date: 2018-12-13 11:10:30
categories: markdown
tags:
  - Markdown
---

开始使用Hexo + GitHub搭建个人博客可以参考有下面这篇文章：
[Hexo + GitHub搭建个人博客](https://www.jianshu.com/p/eded1dd2d794)

[Hexo文档](https://hexo.io/zh-cn/docs/)
[Hexo主题](https://hexo.io/themes/)

## 开始

使用 npm 安装 Hexo:
  `$ npm install -g hexo-cli`

所用主题：matery
`git clone https://github.com/blinkfox/hexo-theme-matery.git`

切换主题
修改 Hexo 根目录下的_config.yml的theme的值：theme: hexo-theme-matery

### Hexo常用命令

`$ hexo generate (hexo g) 生成静态文件`
`$ hexo server (hexo s) 启动本地服务`
`$ hexo deploy (hexo d) 提交到远程仓库`
`$ hexo new page "xx"(hexo n page) 创建页面` 
`$ hexo new "xx" (hexo n "") 创建文章`
`$ hexo d -g 生成静态并提交到远程仓库`
`$ hexo s -g 生成静态文件并启动本地预览`
`$ hexo clean 清除本地 public 文件`
