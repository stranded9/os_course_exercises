# lec1: 操作系统概述

---

## **提前准备**

（请在上课前完成）

* 完成lec1的视频学习和提交对应的在线练习
* git pull ucore\_os\_lab, ucore\_os\_docs, os\_tutorial\_lab, os\_course\_exercises in github repos。这样可以在本机上完成课堂练习。
* 知道OS课程的入口网址，会使用在线视频平台，在线练习/实验平台，在线提问平台\(piazza\)
  * [http://os.cs.tsinghua.edu.cn/oscourse/OS2019spring](http://os.cs.tsinghua.edu.cn/oscourse/OS2019spring)


* 会使用linux shell命令，如ls, rm, mkdir, cat, less, more, gcc等，也会使用linux系统的基本操作。
* 在piazza上就学习中不理解问题进行提问。



# 思考题

## 填空题

* 当前常见的操作系统主要用__C、C++、汇编__编程语言编写。
* "Operating system"这个单词起源于__Operator__ 。
* 在计算机系统中，控制和管理__各种资源__ 、有效地组织__多道程序__运行的系统软件称作__操作系统__ 。
* 允许多用户将若干个作业提交给计算机系统集中处理的操作系统称为__批处理__操作系统
* 你了解的当前世界上使用最多的操作系统是__Android__ 。
* 应用程序通过__系统调用__接口获得操作系统的服务。
* 现代操作系统的特征包括__并发性__ ， __共享性__ ， __虚拟性__ ，__异步性__ 。
* 操作系统内核的架构包括__宏内核结构__ ， __微内核结构__ ， __外核结构__ 。


## 问答题

- 请总结你认为操作系统应该具有的特征有什么？并对其特征进行简要阐述。
  - 并发性：操作系统中可能同时运行着多个程序，需要操作系统对其进行维护（管理和调度）。
  - 共享性：多个程序并发运行的时候操作系统需要做到宏观上“同时”访问资源，但实际微观上互斥。
  - 虚拟性：利用多道程序设计技术，让用户感觉不到多用户的同时使用。
  - 异步性：只要运行环境相同，操作系统需要保证程序运行的结果相同。


- 为什么现在的操作系统基本上用C语言来实现？为什么没有人用python，java来实现操作系统？

  - 因为虽然都是高级语言，python和java相对于C语言来说不够低层，它们的运行实现过程中可能还会调用其他语言，因此不能很好的保证运行的效率。而对于计算机系统来说操作系统的运行效率是至关重要的，会影响到整个机器的使用效率。

---

## 可选练习题

---

- 请分析并理解[v9\-computer](https://github.com/chyyuu/os_tutorial_lab/blob/master/v9_computer/docs/v9_computer.md)以及模拟v9\-computer的em.c。理解：在v9\-computer中如何实现时钟中断的；v9 computer的CPU指令，关键变量描述有误或不全的情况；在v9\-computer中的跳转相关操作是如何实现的；在v9\-computer中如何设计相应指令，可有效实现函数调用与返回；OS程序被加载到内存的哪个位置,其堆栈是如何设置的；在v9\-computer中如何完成一次内存地址的读写的；在v9\-computer中如何实现分页机制。


- 请编写一个小程序，在v9-cpu下，能够输出字符


- 输入的字符并输出你输入的字符


- 请编写一个小程序，在v9-cpu下，能够产生各种异常/中断


- 请编写一个小程序，在v9-cpu下，能够统计并显示内存大小



- 请分析并理解[RISC-V CPU](http://www.riscvbook.com/chinese/)以及会使用模拟RISC\-V(简称RV)的qemu工具。理解：RV的特权指令，CSR寄存器和在RV中如何实现时钟中断和IO操作；OS程序如何被加载运行的；在RV中如何实现分页机制。
  - 请编写一个小程序，在RV下，能够输出字符
  - 输入的字符并输出你输入的字符
  - 请编写一个小程序，在RV下，能够产生各种异常/中断
  - 请编写一个小程序，在RV下，能够统计并显示内存大小
