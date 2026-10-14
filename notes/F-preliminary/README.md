# F 阶段：前置学习

从数电基础一路走到"能自己搭出一台跑得动指令的处理器"。官方预估 39 小时，这一段全在 Logisim 里，还不用写代码。

## 任务清单

| 序号 | 任务 | 预估 |
|:---:|---|:---:|
| F1 | 如何科学地提问 | 2h |
| F2 | Logisim 安装和使用 | 2h |
| F3 | 数字逻辑电路基础 | 20h |
| F4 | 计算机系统的状态机模型 | 5h |
| F5 | 支持数列求和的简单处理器 | 5h |
| F6 | 功能完备的迷你 RISC-V 处理器 | 5h |

## 每项在做什么

F1 讲的是提问的方式：提问前先自己搜（STFW）、先读文档（RTFM）、先读代码（RTFSC），实在卡住了再把"我试了什么、结果是什么、我猜问题出在哪"讲清楚。2 小时基本是看视频的时间，剩下的是习惯问题。

F2 是把 Logisim 装起来，熟悉元件库和连线操作。

F3 是这一段的大头，20 小时。先布尔代数和逻辑门，然后组合逻辑电路（编码器、译码器、多路选择器、加法器），再往上是时序逻辑电路（触发器、寄存器、计数器）和有限状态机。讲义要求门电路都用晶体管级别的元件搭，所以会在 Logisim 的 Wiring 库里跟晶体管打好一阵交道。

F4 讲"程序其实也是状态机"这个视角：一条指令的执行就是一次状态转移。这套想法后面写 NEMU 的时候会一直用。

F5 用 Logisim 搭一个能算数列求和的简单处理器，第一次完整走一遍取指令、译码、执行，也会碰到数据通路和控制器该怎么分。

F6 是把 F5 那个处理器扩成支持 RISC-V 基本指令的版本，为后面用 Verilog 写处理器铺路。

## 笔记

目前建了 F1、F2、F3 三个笔记文件，F4 之后的还没开始写。

## 电路

F3 画的电路都在 [code/logisim/](../../code/logisim/) 下面。

## 讲义和课件

F1 [讲义](https://ysyx.oscc.cc/docs/2407/f/1.html)｜[课件](https://ysyx.oscc.cc/slides/2407/01.html#/)｜[视频](https://www.bilibili.com/video/BV1WvHazNEsk/)

F2 [讲义](https://ysyx.oscc.cc/docs/2407/f/2.html)

F3 [讲义](https://ysyx.oscc.cc/docs/2407/f/3.html)｜[课件上](https://ysyx.oscc.cc/slides/2407/02.html#/)｜[课件下](https://ysyx.oscc.cc/slides/2407/03.html#/)｜[视频上](https://www.bilibili.com/video/BV19nWNz2EZC)｜[视频下](https://www.bilibili.com/video/BV1xentzxED7)

F4 [讲义](https://ysyx.oscc.cc/docs/2407/f/4.html)｜[课件](https://ysyx.oscc.cc/slides/2407/04.html#/)｜[视频](https://www.bilibili.com/video/BV17Lx6zREH6)

F5 [讲义](https://ysyx.oscc.cc/docs/2407/f/5.html)｜[课件](https://ysyx.oscc.cc/slides/2407/05.html#/)｜[视频](https://www.bilibili.com/video/BV1YgxCzdEvq)

F6 [讲义](https://ysyx.oscc.cc/docs/2407/f/6.html)
