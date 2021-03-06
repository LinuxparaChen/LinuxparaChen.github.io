---
layout: post
title: NDK概念及Android Studio下NDK配置
date: 2017-10-09 16:54
comments: true
external-url:
categories: NDK/JNI
---
#### 1.什么是NDK
Native Development Kit 本地开发工具包
#### 2.什么是JNI
Java Native Interface JNI是java和C/C++互相调用的一套规范  
NDK是基于JNI一套工具库
#### 3.为什么使用NDK
1. 性能／效率
2. 安全
3. 便于移植
4. C/C++一些优秀开源库可以直接供java使用

#### 4.NDK配置
1. 下载CMake，LLDB，NDK（需要翻墙，梯子自备）<br>
![](https://github.com/LinuxparaChen/LinuxparaChen.github.io/raw/master/assets/AS-config-NDK-1.png)
2. 配置SDK，JDK，NDK路径，如下图<br>
![](https://github.com/LinuxparaChen/LinuxparaChen.github.io/raw/master/assets/AS-config-NDK-2.png)
3. 新建工程，步骤和普通工程一样，不一样的地方下图会标明<br>
	3.1. 勾选include C++ support<br>
	![](https://github.com/LinuxparaChen/LinuxparaChen.github.io/raw/master/assets/AS-config-NDK-3.png)<br>
	3.2. 勾选Exceptions Support(-fexceptions)/支持异常<br>
		  勾选Runtime Type Information Support(-frtti)/支持运行时类型信息（多态类型转换）<br>
	![](https://github.com/LinuxparaChen/LinuxparaChen.github.io/raw/master/assets/AS-config-NDK-4.png)<br>
4. 一个支持C/C++的工程就完成了。
5. jniLibs目录设置

```
android {
    ...
    defaultConfig {
        ...
        externalNativeBuild {
            cmake {
            	//支持运行时类型信息和C++异常信息
                cppFlags "-frtti -fexceptions"
            }
        }

    }
    ...
    //设置cmake文件路径
    externalNativeBuild {
        cmake {
            path "CMakeLists.txt"
        }
    }
    //设置.so、libs路径
    sourceSets.main {
        jniLibs.srcDirs = ['libs']
        jni.srcDirs = []
    }
}
```