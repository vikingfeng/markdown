---
title: position扩展
date: 2018-12-20 14:55:40
categories: css
tags: 
     - position
---

## absolute之“无依赖绝对定位”

![实现方法](/images/position/t1.png "absolute")
``` html
<img src="https://demo.cssworld.cn/images/6/top1.png" class="top1">
<img src="/images/doraemon.jpg">
.top1 {
  position: absolute;
}
```
### “无依赖绝对定位”-应用场景示例

1. 各类图标定位
   [导航文字右上角图标](https://demo.cssworld.cn/6/5-5.php)
![实现方法](/images/position/t2.png "导航文字右上角图标")
优点： 
   * 如果后面不需要这个图标了，只需要把图标相应的html代码和CSS删掉就可以，文字那些原来的代码不用改动（代码简洁、维护方便）
   * 导航文字长度变化时，图标依然定位良好

2. 超越常规布局的排版
   
3. 下拉列表的定位
   
4. 占位符效果模拟
