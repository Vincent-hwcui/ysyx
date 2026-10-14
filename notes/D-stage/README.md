# D 阶段：正式学习

这一段开始从"画电路"转到"写软件 + 写 RTL"，前后要写的东西比较多。官方预估 34 小时。

## 任务清单

| 序号 | 任务 | 预估 |
|:---:|---|:---:|
| D1 | 支持 RV32IM 的 NEMU | 10h |
| D2 | 程序的机器级表示 | 4h |
| D3 | AM 运行时环境 | 5h |
| D4 | 用 RTL 实现迷你 RISC-V 处理器 | 5h |
| D5 | 设备和输入输出 | 10h |

## 每项在做什么

D1 是把 NEMU 这个指令集模拟器补到能跑 RV32IM，也就是在 RV32I 的基础上加乘除法扩展。后面 D 阶段验证处理器对不对，靠的就是拿 NEMU 当参考做差分测试，所以这一步必须写扎实。

D2 讲程序的机器级表示：汇编和机器码怎么对应、反汇编怎么看、编译器生成的汇编该从哪读起。4 小时，重点是把"看汇编"这件事变成习惯。

D3 是 AM，一层很薄的抽象机器运行时。它做的事情是给程序提供一套统一的接口，让同一份程序既能跑在 NEMU 上、也能跑在真正自己写的处理器上。硬件抽象层这个分层想法从这一项开始成形。

D4 是用 RTL 实现一个迷你 RISC-V 处理器，第一次真正把处理器写成 Verilog。写完要跟 NEMU 做差分测试，逐步把指令一条条对上。

D5 讲设备和输入输出：内存映射 IO（MMIO）是怎么回事、UART 这类基本设备怎么接、处理器和设备之间怎么交互。

## 笔记

还没开始写。

## 代码

NEMU 在 [code/nemu/](../../code/nemu/)，AM 在 [code/am/](../../code/am/)，处理器 RTL 在 [code/npc/](../../code/npc/)。

## 讲义和课件

D1 [讲义](https://ysyx.oscc.cc/docs/2407/d/1.html)｜[课件](https://ysyx.oscc.cc/slides/2407/16.html#/)｜[视频](https://www.bilibili.com/video/BV1RVmMBaEC6)

D2 [讲义](https://ysyx.oscc.cc/docs/2407/d/2.html)｜[课件上](https://ysyx.oscc.cc/slides/2306/09.html#/)｜[课件下](https://ysyx.oscc.cc/slides/2306/10.html#/)

D3 [讲义](https://ysyx.oscc.cc/docs/2407/d/3.html)｜[课件](https://ysyx.oscc.cc/slides/2306/11.html#/)｜[视频](https://www.bilibili.com/video/BV1Vu4y1s73Y)

D4 [讲义](https://ysyx.oscc.cc/docs/2407/d/4.html)

D5 [讲义](https://ysyx.oscc.cc/docs/2407/d/5.html)｜[课件](https://ysyx.oscc.cc/slides/2306/15.html#/)｜[视频](https://www.bilibili.com/video/BV1sb4y1g7Xu)

[D 阶段流片准备与考核](https://ysyx.oscc.cc/docs/2407/d/6.html)
