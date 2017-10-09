---
layout: post
title: Android Studio下NDK配置
date: 207-10-09 09:57
comments: true
external-url:
categories: NDK/JNI
---

1. 下载CMake，LLDB，NDK（需要翻墙，梯子自备）<br>
![CMake，LLDB，NDK下载](https://github.com/LinuxparaChen/LinuxparaChen.github.io/blob/master/assets/AS%E9%85%8D%E7%BD%AENDK-1.png)
2. 配置SDK，JDK，NDK路径，如下图<br>
![配置SDK，JDK，NDK路径](../assets/AS配置NDK-2.png)
3. 新建工程，步骤和普通工程一样，不一样的地方下图会标明<br>
	3.1. 勾选include C++ support<br>
	![新建工程步骤一](../assets/AS配置NDK-3.png)<br>
	3.2. 勾选Exceptions Support(-fexceptions)/支持异常<br>
		  勾选Runtime Type Information Support(-frtti)/支持运行时类型信息（多态类型转换）<br>
	![新建工程步骤二](../assets/AS配置NDK-4.png)<br>
4. 一个支持C/C++的工程就完成了。
