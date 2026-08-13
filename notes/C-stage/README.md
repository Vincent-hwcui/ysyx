# C 阶段：处理器实现

> 用工具和基础设施支持单周期 NPC 处理器，掌握调试技巧、ELF 格式、异常处理和 RT-Thread。

## 阶段任务

| 任务 | 内容 | 预估时间 | 状态 |
|:---:|------|:---:|:---:|
| C1 | 工具和基础设施 | 5h | 🔲 |
| C2 | 支持 RV32E 的单周期 NPC | 5h | 🔲 |
| C3 | 调试技巧 | 2h | 🔲 |
| C4 | ELF 文件和链接 | 2h | 🔲 |
| C5 | 异常处理和 RT-Thread | 15h | 🔲 |
| — | C 阶段结业准备与考核 | — | 🔲 |

## 详细内容

### C1 — 工具和基础设施
- 搭建 NPC（New Processor Core）开发框架
- 差分测试（difftest）框架搭建
- 自动化测试脚本

### C2 — 支持 RV32E 的单周期 NPC
- 实现单周期 RISC-V 处理器（支持 RV32E）
- 与 NEMU 进行差分测试
- 这是从 Logisim 到 Verilog 的重要跨越

### C3 — 调试技巧
- 掌握波形调试（GTKWave）
- 掌握 GDB 调试
- 学会定位处理器 bug

### C4 — ELF 文件和链接
- 理解 ELF 文件格式
- 理解链接过程
- 学会让处理器运行 ELF 程序

### C5 — 异常处理和 RT-Thread（核心）
- 理解 RISC-V 异常/中断机制
- 实现 CSR 寄存器（mcause、mstatus、mtvec 等）
- 让 RT-Thread 操作系统运行在自己的处理器上
- 这是处理器"能跑操作系统"的关键一步

## 笔记文件

- `C1-infrastructure.md` — 工具和基础设施笔记
- `C2-single-cycle-npc.md` — 单周期 NPC 笔记
- `C3-debugging.md` — 调试技巧笔记
- `C4-elf-link.md` — ELF 和链接笔记
- `C5-exception-rtthread.md` — 异常处理和 RT-Thread 笔记

## 代码位置

- NPC 处理器: [code/npc/](../../code/npc/)

## 讲义与资源

- [C1 讲义](https://ysyx.oscc.cc/docs/2407/c/1.html) | [课件](https://ysyx.oscc.cc/slides/2306/12.html#/) | [视频](https://www.bilibili.com/video/BV1RM411Q7Au)
- [C2 讲义](https://ysyx.oscc.cc/docs/2407/c/2.html) | [课件](https://ysyx.oscc.cc/slides/2306/13.html#/) | [视频](https://www.bilibili.com/video/BV1rc411f7mK)
- [C3 讲义](https://ysyx.oscc.cc/docs/2407/c/3.html) | [课件](https://ysyx.oscc.cc/slides/2306/16.html#/) | [视频](https://www.bilibili.com/video/BV1Vz4y1A7Rt)
- [C4 讲义](https://ysyx.oscc.cc/docs/2407/c/4.html) | [课件](https://ysyx.oscc.cc/slides/2306/14.html#/) | [视频](https://www.bilibili.com/video/BV1Ly4y1w7hn)
- [C5 讲义](https://ysyx.oscc.cc/docs/2407/c/5.html) | [课件](https://ysyx.oscc.cc/slides/2306/17.html#/) | [视频](https://www.bilibili.com/video/BV1734y1w7ro)
