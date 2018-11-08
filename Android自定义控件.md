---
title: Android自定义控件 
tags: Android,UIView与视图
grammar_cjkRuby: true
---

[toc]

 ## 绘图基础
 
 ### 基本图形绘制
 
**Paint类——画笔**

设置属性：粗细，颜色，透明度，字体样式等等

**Canvas类——画布**

设置图形形状：圆形，矩形，文字等等

**自定义控件**

继承View——类似Button、TextView

**自定义容器**

继承ViewGroup——类似RelativeLayout、LinearLayout

**流程**
1. 继承View，必须继承构造方法否则在xml文件中引用会出错
2. 重写onDraw()方法
3. 在onDraw()方法中设置Paint,并调用Canvas的绘图方法

**Paint.style**
1. Style有效时，StrokeWidth用于设置描边宽度
2. Style无效时，StrokeWidth用于设置画笔宽度


