# 学习路线图（官方 v24.07 版）

官方把整个计划分成 F → E → D → C → B → A → S 七个阶段，必须一个阶段过了考核才能进下一个，跳不了级。课程主页在 <https://ysyx.oscc.cc/docs/2407/>。

## 各阶段的任务和时间

下面这张表是按官方记录表整理的，时间是官方给的预估。

| 阶段 | 任务 | 预估 |
|:---:|:---|:---:|
| F | F1 如何科学地提问 | 2h |
| | F2 Logisim 安装和使用 | 2h |
| | F3 数字逻辑电路基础 | 20h |
| | F4 计算机系统的状态机模型 | 5h |
| | F5 支持数列求和的简单处理器 | 5h |
| | F6 功能完备的迷你 RISC-V 处理器 | 5h |
| E | E1 C 语言程序设计 | 20h |
| | E2 硬件描述语言 | 20h |
| | E3 Linux 系统安装和基本使用 | 10h |
| | E4 从 C 代码到二进制程序 | 10h |
| | E5 RTL 代码的仿真 | 20h |
| | E6 完成 PA1 | 20h |
| | 申请入学答辩 | — |
| D | D1 支持 RV32IM 的 NEMU | 10h |
| | D2 程序的机器级表示 | 4h |
| | D3 AM 运行时环境 | 5h |
| | D4 用 RTL 实现迷你 RISC-V 处理器 | 5h |
| | D5 设备和输入输出 | 10h |
| C | C1 工具和基础设施 | 5h |
| | C2 支持 RV32E 的单周期 NPC | 5h |
| | C3 调试技巧 | 2h |
| | C4 ELF 文件和链接 | 2h |
| | C5 异常处理和 RT-Thread | 15h |
| B | B1 总线 | 10h |
| | B2 SoC 计算机系统 | 30h |
| | B3 时序分析和优化 | 5h |
| | B4 性能优化和简易缓存 | 20h |
| | B5 流水线处理器 | 20h |
| A | A1 乘除法器、A2 系统调用、A3 虚存管理、A4 特权级和 xv6、A5 启动 Linux、A6 缓存进阶、A7 分支预测进阶 | — |
| S | 待官方发布 | — |

F 到 B 加起来 287 小时，其中 E 和 B 各占将近三分之一。

## 关于时间

官方这些预估是按"中等水平"算的——他们的定义是学习态度端正、写过 500 行以上的单个程序、会调试，不是指程序设计课考了多少分。如果是零基础，官方说预期要花 2~3 倍的时间。

另外官方明确讲了学习以讲义为主，课件和视频是辅助资源，所以不用想着把视频全刷完。

A 阶段的预估时间官方还留空着，讲义也没出全，等更新了再补。

## 各阶段的详细笔记

F 在 [notes/F-preliminary](../notes/F-preliminary/README.md)，E 在 [notes/E-entry](../notes/E-entry/README.md)，D 在 [notes/D-stage](../notes/D-stage/README.md)，C 在 [notes/C-stage](../notes/C-stage/README.md)，B 在 [notes/B-stage](../notes/B-stage/README.md)，A 在 [notes/A-stage](../notes/A-stage/README.md)。学习资源的汇总见 [resources.md](./resources.md)。
