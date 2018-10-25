---
title: iOS学习笔记
tags: swift3.0, UIView与视图
grammar_cjkRuby: true
---
## 标签与按钮

1. Button的Connection设置为Action
2. 代码实现Button的事件处理：通过UIControl类的addTarget()
3. Label的Connection设置为Qutlet
4. Label标签自适应文本内容,需要在设置text内容之后调用
```swift
	label.sizeToFit()
```
5. 在swift中默认属性是Strong，在Interface Builder中是weak，因为：
Interface Builder实现label等视图是在故事板中定义的，当应用程序启动时会根据故事板的描述创建label等视图对象，对象所有权在故事板，它们对label等视图对象是强引用的。由于对象所有权不是视图控制器，所以在视图控制器中使用它hi不能一味strong,只能定义为weak.

## TextField和TextView

 - 与Label的区别：
	- TextField和TextView可以设置键盘
	- TextField和TextView各有一个委托协议 
 - TextField和TextView的区别：
	- TextField由UITextField类创建，UITextField继承UIControl，属于控件
	- TextView由UITextView类创建，UITextView继承UIScrollVIew,不属于控件
 - 需要将ViewController当前对象复制给TextView和TextField控件的delegate委托属性，否则委托协议中的方法不会被调用，此过程可以通过代码或者Interface Builder完成
 - TextField和TextView获取焦点时，成为了“第一响应者”,不同视图成为“第一响应者”的表现不太一致，TextField和TextView等输入类型的空间会表现出弹出软键盘，所以要关闭软件然的方法，就是放弃“第一响应者”：
```swift
	textField.resignFirstResponder()
	textView.resignFirstResponder()
```
5.键盘打开和关闭的监听通知：
 - 

