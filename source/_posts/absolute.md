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

## absolute的流体特性

* 无论设置padding还是margin，其占据的空间一直不变，变化的就是content box的尺寸，这就是典型的流体表现特性。
* 对立方向同时发生定位时，绝对定位元素具有流体特性

## relative

* relative定位两大特性： **相对自身、无侵入**
* relative的left/right/top/bottom的值为数字是，定位位移相对于自身，但是值为百分比时是相对于包含块计算的。
* 相对定位元素同时应用对立方向定位值时，**只有一个方向的定位属性起作用**，跟**文档流的顺序**有关（默认的文档流是自上而下、从左往右），所以top/bottom同时使用时，只有top生效，left/right同时使用时，只有left生效。

## relative最小化影响原则

* 尽量不使用relative，可以考虑能不能用“无依赖的绝对定位”
* 如果一定要用，则该relative务必最小化。