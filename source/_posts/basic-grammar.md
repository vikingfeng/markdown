---
title: 初学markdown
date: 2018-12-13 11:40:30
categories: markdown知识
tags: 
     - markdown
---
---

## 基础语法  

链接 :[Hexo主题](https://hexo.io/themes/)
**加粗** : `**Bold**`
*斜体字* : `*斜体*`
***加粗+斜体***：`***斜体加粗***`
~~删除线~~：`~~这是加删除线的文字~~`
高亮 :==text==
段落 : 段落之间空一行
换行符 : 一行结束时输入两个空格
内嵌代码 : `alert('Hello World');`
方框：- [ ] -


## 引用  

在引用的文字前加>即可。引用也可以嵌套，如加两个>>三个>>>
n个...
貌似可以一直加下去，但没神马卵用
![引用](/images/markdown/reference.png "引用")
示例：
>这是引用的内容
>>这是引用的内容
>>>>>>>>>>这是引用的内容
---

## 分割线  

三个或者三个以上的 - 或者 * 都可以。
![分割线](/images/markdown/dividing-line.png "分割线")

---
----
***
*****
---

## 图片

`![图片alt](图片地址 ''图片title'')`
`图片alt就是显示在图片下面的文字，相当于对图片内容的解释。`
`图片title是图片的标题，当鼠标移到图片上时显示的内容。title可加可不加`
eg: ![哆啦A梦](/images/doraemon.jpg "哆啦A梦")

## 超链接

`[超链接名](超链接地址 "超链接title") title可加可不加`
eg:
[Hexo文档](https://hexo.io/zh-cn/docs/)
[Melody](https://molunerfinn.com/)

## 注释

![有序列表](/images/markdown/comment.png "有序列表")

1. html标签（你如果看不到下面的注释说明已经成功注释）  

    <div style='display: none'>哈哈我是注释，不会在浏览器中显示。我也是注释。</div>

2. html注释（你如果看不到下面的注释说明已经成功注释）  

<!--哈哈我是注释，不会在浏览器中显示。-->
<!--
哈哈我是多行
注释，
不会在浏览器中显示。
-->

3. hack注释（你如果看不到下面的注释说明已经成功注释)  

[^_^]: # (哈哈我是注释，不会在浏览器中显示。)

---
