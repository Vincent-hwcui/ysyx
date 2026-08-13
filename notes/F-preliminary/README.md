# F 阶段：前置学习

> 数字电路与处理器设计入门，为正式学习打基础。

## 阶段任务

| 任务 | 内容 | 预估时间 | 状态 |
|:---:|------|:---:|:---:|
| F1 | 如何科学地提问 | 2h | ✅ |
| F2 | Logisim 安装和使用 | 2h | ✅ |
| F3 | 数字逻辑电路基础 | 20h | 🔲 |
| F4 | 计算机系统的状态机模型 | 5h | 🔲 |
| F5 | 支持数列求和的简单处理器 | 5h | 🔲 |
| F6 | 功能完备的迷你 RISC-V 处理器 | 5h | 🔲 |

## 详细内容

### F1 — 如何科学地提问
- 学会提问的 SMART 原则
- 学会使用搜索引擎和文档
- 学会在社区高效求助

### F2 — Logisim 安装和使用
- 安装 Logisim（数字电路模拟器）
- 熟悉基本元件和连线操作

### F3 — 数字逻辑电路基础（核心）
- 布尔代数与逻辑门
- 组合逻辑电路（编码器、译码器、多路选择器、加法器）
- 时序逻辑电路（触发器、寄存器、计数器）
- 有限状态机 (FSM)
- **用 Logisim 搭建电路**

### F4 — 计算机系统的状态机模型
- 理解"程序 = 状态机"的核心思想
- 指令的执行是状态转移的过程
- 为后续 NEMU 模拟器设计奠定理论基础

### F5 — 支持数列求和的简单处理器
- 用 Logisim 设计一个能计算数列求和的简单处理器
- 理解数据通路和控制器
- 第一次完整经历"指令→执行"的流程

### F6 — 功能完备的迷你 RISC-V 处理器
- 在 Logisim 中实现一个支持 RISC-V 核心指令的处理器
- 支持 I 型、R 型等基本指令格式
- 为后续用 Verilog 实现处理器打基础

## 笔记文件

- `F1-question.md` — 科学提问笔记
- `F2-logisim.md` — Logisim 使用笔记
- `F3-digital-logic.md` — 数字逻辑电路笔记
- `F4-fsm-model.md` — 状态机模型笔记
- `F5-simple-processor.md` — 简单处理器设计笔记
- `F6-mini-riscv.md` — 迷你 RISC-V 处理器笔记

## 代码位置

- Logisim 电路文件: [code/logisim/](../../code/logisim/)

## 讲义与资源

- [F1 讲义](https://ysyx.oscc.cc/docs/2407/f/1.html) | [课件](https://ysyx.oscc.cc/slides/2407/01.html#/) | [视频](https://www.bilibili.com/video/BV1WvHazNEsk/)
- [F2 讲义](https://ysyx.oscc.cc/docs/2407/f/2.html)
- [F3 讲义](https://ysyx.oscc.cc/docs/2407/f/3.html) | [课件上](https://ysyx.oscc.cc/slides/2407/02.html#/) | [课件下](https://ysyx.oscc.cc/slides/2407/03.html#/) | [视频上](https://www.bilibili.com/video/BV19nWNz2EZC) | [视频下](https://www.bilibili.com/video/BV1xentzxED7)
- [F4 讲义](https://ysyx.oscc.cc/docs/2407/f/4.html) | [课件](https://ysyx.oscc.cc/slides/2407/04.html#/) | [视频](https://www.bilibili.com/video/BV17Lx6zREH6)
- [F5 讲义](https://ysyx.oscc.cc/docs/2407/f/5.html) | [课件](https://ysyx.oscc.cc/slides/2407/05.html#/) | [视频](https://www.bilibili.com/video/BV1YgxCzdEvq)
- [F6 讲义](https://ysyx.oscc.cc/docs/2407/f/6.html)
