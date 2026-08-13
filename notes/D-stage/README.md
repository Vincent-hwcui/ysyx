# D 阶段：正式学习

> 完善 NEMU 模拟器，理解程序机器级表示，用 RTL 实现迷你 RISC-V 处理器，掌握设备与 IO。

## 阶段任务

| 任务 | 内容 | 预估时间 | 状态 |
|:---:|------|:---:|:---:|
| D1 | 支持 RV32IM 的 NEMU | 10h | 🔲 |
| D2 | 程序的机器级表示 | 4h | 🔲 |
| D3 | AM 运行时环境 | 5h | 🔲 |
| D4 | 用 RTL 实现迷你 RISC-V 处理器 | 5h | 🔲 |
| D5 | 设备和输入输出 | 10h | 🔲 |
| — | D 阶段流片准备与考核 | — | 🔲 |

## 详细内容

### D1 — 支持 RV32IM 的 NEMU
- 完善 NEMU（NJU Emulator）指令集模拟器
- 支持 RV32IM 指令集（含乘除法扩展）
- 为后续差分测试（difftest）打基础

### D2 — 程序的机器级表示
- 理解汇编与机器码的对应关系
- 掌握反汇编技巧
- 学会阅读编译器生成的汇编代码

### D3 — AM 运行时环境
- AM（Abstract Machine）抽象机器运行时
- 理解硬件抽象层（HAL）的设计思想
- 让程序能在不同"机器"上运行

### D4 — 用 RTL 实现迷你 RISC-V 处理器（核心）
- 用 Verilog 实现一个迷你 RISC-V 处理器
- 与 NEMU 进行差分测试验证正确性
- 这是第一次"真正的处理器 RTL 实现"

### D5 — 设备和输入输出
- 理解内存映射 IO (MMIO)
- 实现 UART 串口等基本设备
- 处理器与设备的交互

## 笔记文件

- `D1-nemu-rv32im.md` — NEMU 完善笔记
- `D2-machine-representation.md` — 机器级表示笔记
- `D3-am.md` — AM 运行时环境笔记
- `D4-mini-riscv-rtl.md` — 迷你 RISC-V RTL 实现笔记
- `D5-device-io.md` — 设备与 IO 笔记

## 代码位置

- NEMU 模拟器: [code/nemu/](../../code/nemu/)
- AM 运行时: [code/am/](../../code/am/)
- 处理器 RTL: [code/npc/](../../code/npc/)

## 讲义与资源

- [D1 讲义](https://ysyx.oscc.cc/docs/2407/d/1.html) | [课件](https://ysyx.oscc.cc/slides/2407/16.html#/) | [视频](https://www.bilibili.com/video/BV1RVmMBaEC6)
- [D2 讲义](https://ysyx.oscc.cc/docs/2407/d/2.html) | [课件上](https://ysyx.oscc.cc/slides/2306/09.html#/) | [课件下](https://ysyx.oscc.cc/slides/2306/10.html#/)
- [D3 讲义](https://ysyx.oscc.cc/docs/2407/d/3.html) | [课件](https://ysyx.oscc.cc/slides/2306/11.html#/) | [视频](https://www.bilibili.com/video/BV1Vu4y1s73Y)
- [D4 讲义](https://ysyx.oscc.cc/docs/2407/d/4.html)
- [D5 讲义](https://ysyx.oscc.cc/docs/2407/d/5.html) | [课件](https://ysyx.oscc.cc/slides/2306/15.html#/) | [视频](https://www.bilibili.com/video/BV1sb4y1g7Xu)
- [D 阶段流片准备与考核](https://ysyx.oscc.cc/docs/2407/d/6.html)
