# C 阶段：处理器实现

这一段的目标是让自己的处理器能跑起操作系统。官方预估 29 小时，其中 C5 一个人占一半。

## 任务清单

| 序号 | 任务 | 预估 |
|:---:|---|:---:|
| C1 | 工具和基础设施 | 5h |
| C2 | 支持 RV32E 的单周期 NPC | 5h |
| C3 | 调试技巧 | 2h |
| C4 | ELF 文件和链接 | 2h |
| C5 | 异常处理和 RT-Thread | 15h |

## 每项在做什么

C1 是搭 NPC 的开发框架：差分测试怎么跑起来、自动化测试脚本怎么写。这一项本身不难，但后面所有验证都靠它，所以得先弄顺。

C2 是把处理器实现成单周期版本，支持 RV32E 指令集，再跟 NEMU 做差分测试。RV32E 是 RV32I 的缩减版，寄存器少一些，正好适合先把单周期这条数据通路走通。

C3 讲调试：GTKWave 看波形、GDB 断下来看状态，以及怎么一步步把处理器的 bug 定位到具体某条信号上。2 小时，但没这个后面会很痛苦。

C4 是 ELF 文件和链接。要让自己写的处理器能直接跑 ELF 程序，就得弄明白 ELF 里都有什么、链接器把各个段摆到了哪里。

C5 是这一段的重头戏，15 小时：RISC-V 的异常和中断机制、CSR 寄存器（mcause、mstatus、mtvec 这一组）、最后让 RT-Thread 跑在自己的处理器上。能把操作系统跑起来，处理器的基本功能才算真正完整。

## 笔记

还没开始写。

## 代码

NPC 处理器在 [code/npc/](../../code/npc/)。

## 讲义和课件

C1 [讲义](https://ysyx.oscc.cc/docs/2407/c/1.html)｜[课件](https://ysyx.oscc.cc/slides/2306/12.html#/)｜[视频](https://www.bilibili.com/video/BV1RM411Q7Au)

C2 [讲义](https://ysyx.oscc.cc/docs/2407/c/2.html)｜[课件](https://ysyx.oscc.cc/slides/2306/13.html#/)｜[视频](https://www.bilibili.com/video/BV1rc411f7mK)

C3 [讲义](https://ysyx.oscc.cc/docs/2407/c/3.html)｜[课件](https://ysyx.oscc.cc/slides/2306/16.html#/)｜[视频](https://www.bilibili.com/video/BV1Vz4y1A7Rt)

C4 [讲义](https://ysyx.oscc.cc/docs/2407/c/4.html)｜[课件](https://ysyx.oscc.cc/slides/2306/14.html#/)｜[视频](https://www.bilibili.com/video/BV1Ly4y1w7hn)

C5 [讲义](https://ysyx.oscc.cc/docs/2407/c/5.html)｜[课件](https://ysyx.oscc.cc/slides/2306/17.html#/)｜[视频](https://www.bilibili.com/video/BV1734y1w7ro)

[C 阶段结业考核申请](https://ysyx.oscc.cc/docs/2407/c/6.html)
