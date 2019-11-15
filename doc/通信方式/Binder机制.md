前言
====
在看Android音频源码时，从本地框架到AudioPolicyService之间类调用关系不清晰，所以参考网络上的分析学习下android的Binder机制

Binder是android系统的进程间通信机制，linux常见的进程间通信手段IPC（Internet Process Connection）有：信号signal、socket、队列message等

一、Binder是什么？
====


二、知识储备
====

### 2.1 进程空间划分
* 进程空间分为用户空间、内核空间
* 二者区别
  1.进程间，用户空间数据不可共享, 内核空间的数据可共享
  2.所有进程共用一个内核空间
* 一个进程里面，用户空间和内核空间数据交互主要通过系统调用（copy_from_user/copy_to_user），当然也有其他的方式
### 2.2 进程隔离 & 跨进程通信（ IPC ）
* 进程隔离
* 跨进程通信IPC
* 跨进程通信基本原理
  传统跨进程通信需要拷贝2次，即从进程的用户空间->内核缓存区->另一进程用户空间
  而binder使用了[内存映射](https://www.jianshu.com/p/719fc4758813)只需要拷贝一次
### [内存映射](https://www.jianshu.com/p/719fc4758813)  
三、Binder模型
====
### 3.1 模型原理图
 Binder 跨进程通信机制 模型 基于 Client - Server 模式 
 
