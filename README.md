介绍
====
ucore os labs是用于清华大学计算机科学与技术系的操作系统课程实验。

新闻
====
- 2019.03.01: [来自scratch的手把手rcore os labs实验](https://github.com/LearningOS/rcore_step_by_step)正在进行。感谢Qingling Pan，Fengyuan Liu的卓越贡献。
- 2019.01.19: [rcore os labs (pre-alpha版本)](https://github.com/oscourse-tsinghua/rcore_plus/tree/lab8-rv32)在RISC-V(32bit)上的版本已发布。感谢Runji Wang，Wei Zhang，Zhenyang Dai，Jiajie Chen，Yuekai Jia，Cheng Lu等人的卓越贡献。
- 2019.01.19: [rcore os labs (pre-pre-alpha版本)](https://github.com/oscourse-tsinghua/rcore_plus/tree/lab8-aarch64)在树莓派(AARCH 64bit)上的版本已发布。感谢Yuekai Jia，Runji Wang，Jiajie Chen等人的卓越贡献。
- 2018.04.03：ucore os labs完成了到RISC-V(64bit) CPU（privileged arch spec 1.10)的移植。你可以通过[仓库的riscv64-priv-1.10分支](https://github.com/chyyuu/ucore_os_lab/tree/riscv64-priv-1.10)查看。感谢Zhengxing Shi的卓越贡献。
- 2018.03.18: Weixiao Huang提供了https://github.com/weixiao-huang/silver-spoon来支持os labs在windows/macos/linux系统下，在docker环境中的支持。[查看细节](https://github.com/weixiao-huang/silver-spoon/tree/master/docs)
- 2018.02.03：ucore os labs完成了到RISC-V(32bit) CPU（privileged arch spec 1.10)的移植。你可以通过[仓库的riscv32-priv-1.10分支](https://github.com/chyyuu/ucore_os_lab/tree/riscv32-priv-1.10)查看。感谢Wei Zhang的卓越贡献。

维护人员
========

清华大学计算机科学与技术系操作系统课程，以及MOOC的操作系统课程
-----------------------------------
- Chen, Yu: yuchen@tsinghua.edu.cn http://soft.cs.tsinghua.edu.cn/~chen
- Xiang, Yong: xyong@tsinghua.edu.cn
- Mao, Junjie: eternal.n08@gmail.com
- Zhang, Wei: zhangwei15@mails.tsinghua.edu.cn
- Wang, Runji: wangrunji0408@163.com 
- Jia, Yuekai: jiayk15@mails.tsinghua.edu.cn

内容
====

实验基本信息
----------------
```
lab0: 热身准备
lab1: 启动和保护 模式，栈和中断（boot/protect mode/stack/interrupt）
lab2: 物理内存管理
lab3: 虚拟内存管理
lab4: 内核线程管理
lab5: 用户进程管理
lab6: 线程调度（翻译存疑，原文为scheduling）
lab7: 互斥量和同步（mutex/sync）
lab8: 文件系统
```

已测试的环境
============
```
UBUNTU 16.04 x86-64: GCC-7.3 
UBUNTU 14.04+: GCC-4.8.2+ CLANG-3.5+
FEDORA 20+: GCC-4.8.2+
```

练习步骤
========
```
0 获取最新的os lab源码和文档。（确保你可以在vbox虚拟机上运行的ubuntu连接到github）（译者注：本人使用的是VMware）
0.1 如果你希望获取全部源码
  $rm -rf ucore_lab
  $git clone git://github.com/chyyuu/ucore_os_lab.git
  $cd ucore_lab
0.2 如果你克隆了ucore_lab仓库，并且只希望获取升级了的代码
  $cd ucore_os_lab
  $git pull
1 $cd labX
2 阅读源码（尤其是经过增改的文件）
3 加入你的源码
4 编译你的源码
  $make
5 检查你的成果
  $make qemu
或者
  $make grade

6 调试你的源码
  $make debug

7 提交你的源码
  $make handin
```

可选项
======
ucore现已支持LLVM/Clang-3.5 + 
在第四步中：
  $ USELLVM=1 make
然后你就可以用clang编译源码了

评级
====
```
超人：在一个月内独立完成所有实验
大师：在两个月内独立完成所有实验
老兵：在三个月内独立完成所有实验
学徒：在他人帮助下，一个学期（semester）内完成所有实验
```

源码仓库
========
```
基础OS labs （为学习操作系统的学生准备）
查阅最新实验代码和文档： https://github.com/chyyuu/ucore_os_lab

进阶OS labs （为操作系统大佬、骇客，或者是超人、大师级玩家准备）
查阅最新实验代码和文档： https://github.com/chyyuu/ucore_plus
```


UCORERS（贡献者）
==================

Junjie Mao, Yuheng Chen, Cong Liu, Yang Yang, Zhun Qu, Shengwei Ren, Wenlei Zhu, Cao Zhang, Tong Sen, Xu Chen, 
Cang Nan, Yujian Fang, Wentao Han, Kaichen Zhang, Xiaolin Guo, Tianfan Xue, Gang Hu, Cao Liu, Yu Su,Xinhao Yuan, Wei Zhang, Kaixiang Lei等

加入清华大学操作系统研究小组
============================
如果你对操作系统研究或开发有兴趣，清华大学操作系统研究小组欢迎你：
- 多核架构下操作系统性能提升
- 操作系统的fuzzing/符号执行技术，用于发现内核的bug
- 提升操作系统子系统的性能和可靠性，例如设备驱动
- 设计操作系统范式（翻译存疑，原文为specification），生成正确无误的操作系统
- 操作系统和CPU（例如RISC-V）的代码符号（codesign）
- 其他操作系统有关主题

例如[其他激动人心的操作系统研究](https://github.com/chyyuu/aos_course/blob/master/readinglist.md)

请向研究小组发送邮件！

其他信息
========
ucore是一个教学用操作系统，它派生自麻省理工大学的xv6&jos，哈佛大学的OS161以及Linux。

ucore被研发和使用于清华大学计算机科学与技术系交叉信息研究院。

构造了xv6&jos的源码文件版权属于Frans Kaashoek，Robert Morris，以及Russ Cox ，使用MIT许可证，版权自2006年起至现在。

构造了OS/161的源码文件由David A. Holland编写。

构造了ucore的源码文件版权属于Yu Chen，Naizheng Wang，Yong Xiang，使用GPL许可证，版权自2010年起至现在。

构造了ucore的文档版权属于Yu Chen, Yong Xiang，使用Creative Commons Attribution/Share-Alike (CC-BY-SA)许可证，版权自2010年起至现在。

