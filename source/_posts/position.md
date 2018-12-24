---
title: position
date: 2018-12-19 09:30:00
categories: 
    - CSS
tags:
    - position
---

## Position-概念

position的四个属性值：
1. **relative**
2. **absolute**
3. **fixed**
4. **static**

position属性只是使元素脱离文档流，要想此元素能按照希望的位置显示，就需要使用下面的属性(position:static不支持这些)：
①**left** ： 表示向元素的左边插入多少像素，使元素向右移动多少像素。
②**right** ：表示向元素的右边插入多少像素，使元素向左移动多少像素。
③**top** ：表示向元素的上方插入多少像素，使元素向下移动多少像素。
④**bottom** ：表示向元素的下方插入多少像素，使元素向上移动多少像素。
上面属性的值可以为负，单位：px 。

``` css
<div id="parent">
     <div id="square1">square1</div>
     <div id="square2">square2</div>
</div>
```

#### 一、 relative

``` css
.square1{
        position: relative;
        border:5px solid green;
        margin:20px;
        padding:10px;
        top:10px;
       }
```
square1位置：square1如果不设置relative时它应该在哪个位置，一旦设置后就按照它这个位置进行偏移。

那square2的位置又在哪里呢？答案是它原来在哪里，现在就在哪里，它的位置不会因为square1增加了position的属性而发生改变。

如果此时把square2的position也设置为relative，会发生什么现象？此时依然和square1一样，按照它原来应有的位置进行偏移。

* 注意relative的偏移是基于当前对象(如square1)的margin的左上侧的。
* position:relative 对 table-*-group, table-row, table-column, table-cell, table-caption 元素无效。

#### 二、 absolute

1. 当square1的父对象(或曾祖父，只要是父级对象)parent也设置了position属性，且position的属性值为absolute或者relative时，也就是说，不是默认值的情况，此时square1按照这个parent来进行定位。

注意，对象虽然确定好了，但有些细节需要您的注意，那就是我们到底以parent的哪个定位点来进行定位呢？如果parent设定了margin，border，padding等属性，那么这个定位点将忽略padding，将会**从父对象padding开始的地方(即只从padding的左上角开始)进行定位**，这与我们会想当然的以为会以margin的左上端开始定位的想法是不同的。

接下来的问题是，square2的位置到哪里去了呢？由于当**position设置为absolute后，会导致square1溢出正常的文档流，就像它不属于 parent一样，它漂浮了起来**，在DreamWeaver中把它称为“层”，其实意思是一样的。此时square2将获得square1的位置，它的文档流不再基于 square1，而是直接从parent开始。
2. 如果square1不存在一个有着position属性的父对象，那么那就会以body为定位对象，按照浏览器的窗口进行定位，这个比较容易理解。

![a](/images/position/tips.png "a")

#### 三、 fixed

fixed是特殊的absolute，即fixed总是以body为定位对象的，按照浏览器的窗口进行定位。

#### 四、 static

position的默认值，一般不设置position属性时，会按照正常的文档流进行排列。

####  *tips

* 注意relative的偏移是基于对象的margin的左上侧的。
* absolute:定位点将忽略padding，将会从父对象的padding开始的地方(即只从padding的左上角开始)进行定位


**Position**

![absolute](/images/position/absolute.png "absolute")
