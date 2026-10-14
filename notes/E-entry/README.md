# E 阶段：入门学习

从"只会画电路"过渡到"能用代码描述硬件"。官方预估 100 小时，是 F 到 B 里面最重的一段。做完这一段要完成 PA1 并申请入学答辩。

## 任务清单

| 序号 | 任务 | 预估 |
|:---:|---|:---:|
| E1 | C 语言程序设计 | 20h |
| E2 | 硬件描述语言 | 20h |
| E3 | Linux 系统安装和基本使用 | 10h |
| E4 | 从 C 代码到二进制程序 | 10h |
| E5 | RTL 代码的仿真 | 20h |
| E6 | 完成 PA1 | 20h |
| — | 申请入学答辩 | — |

## 每项在做什么

E1 是 C 语言程序设计，20 小时。重点是语法之外的指针、结构体、动态内存管理这些，因为后面写 NEMU 和测试程序全靠它。这一段没配视频，基本靠自己敲。

E2 是硬件描述语言，也是 20 小时。从时序逻辑的思维切换到"用代码描述电路"，写 Verilog 或者 Chisel。同样是自学为主。

E3 讲 Linux 的安装和基本使用，10 小时。装环境（Ubuntu 或者 WSL2）、Shell 命令、vim 和 Makefile 这些。

E4 讲 C 代码怎么变成二进制程序：预处理、编译、汇编、链接这四步各自做了什么，还有指令集模拟器是怎么一条条执行指令的。

E5 是这一段最硬的一块，20 小时。内容多：RTL 代码的仿真（用 Verilator 跑 Verilog）、逻辑综合（RTL 到门级网表）、Verilog 的 RTL 综合语义（哪些写法能综合、哪些不能）、标准单元库、以及物理设计（布局布线的基础）。这一项和 D 阶段的 D6 是连着的。

E6 是完成 NEMU 的 PA1，20 小时，做完之后申请入学答辩。答辩通过才算真正进入 D 阶段。

## 笔记

还没开始写。E 阶段的笔记文件暂时没建。

## 讲义和课件

E1 [讲义](https://ysyx.oscc.cc/docs/2407/e/1.html)

E2 [讲义](https://ysyx.oscc.cc/docs/2407/e/2.html)

E3 [讲义](https://ysyx.oscc.cc/docs/2407/e/3.html)｜[课件](https://ysyx.oscc.cc/slides/2407/06.html#/)｜[视频](https://www.bilibili.com/video/BV1wD4xzbEpU)

E4 [讲义](https://ysyx.oscc.cc/docs/2407/e/4.html)｜[课件](https://ysyx.oscc.cc/slides/2407/07.html#/)｜[视频](https://www.bilibili.com/video/BV1TtWYz2Eun)

E5 [讲义](https://ysyx.oscc.cc/docs/2407/e/5.html)｜[课件](https://ysyx.oscc.cc/slides/2407/10.html#/)｜[视频](https://www.bilibili.com/video/BV1ho1ZBbETt)

E6 [讲义](https://ysyx.oscc.cc/docs/2407/e/6.html)｜[课件](https://ysyx.oscc.cc/slides/2407/15.html#/)｜[视频](https://www.bilibili.com/video/BV1bc2YB9Ehi)

[申请入学答辩](https://ysyx.oscc.cc/docs/2407/e/7.html)
