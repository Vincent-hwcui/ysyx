# B 阶段：SoC 系统设计

> 总线设计、SoC 系统集成、时序分析、缓存优化、流水线处理器。

## 阶段任务

| 任务 | 内容 | 预估时间 | 状态 |
|:---:|------|:---:|:---:|
| B1 | 总线 | 10h | 🔲 |
| B2 | SoC 计算机系统 | 30h | 🔲 |
| B3 | 时序分析和优化 | 5h | 🔲 |
| B4 | 性能优化和简易缓存 | 20h | 🔲 |
| B5 | 流水线处理器 | 20h | 🔲 |
| — | B 阶段流片准备与考核 | — | 🔲 |

## 详细内容

### B1 — 总线
- 总线协议（AXI / AXI-Lite）
- 总线互联（Crossbar / 共享总线）
- 主从设备通信

### B2 — SoC 计算机系统（核心，时间最长）
- 将 NPC 处理器集成为完整 SoC
- 集成 SRAM、ROM、UART、SPI 等外设
- 地址空间映射
- 中断控制器
- 在 FPGA 上运行完整系统

### B3 — 时序分析和优化
- 静态时序分析 (STA)
- 关键路径优化
- 时序约束

### B4 — 性能优化和简易缓存
- 实现简易 Cache
- 理解局部性原理
- 缓存性能分析

### B5 — 流水线处理器
- 将单周期 NPC 改造为流水线处理器
- 冒险检测与处理（转发、停顿）
- 流水线性能分析

## 笔记文件

- `B1-bus.md` — 总线笔记
- `B2-soc.md` — SoC 系统笔记
- `B3-timing.md` — 时序分析笔记
- `B4-cache.md` — 缓存笔记
- `B5-pipeline.md` — 流水线笔记

## 代码位置

- SoC 系统: [code/npc/](../../code/npc/)（SoC 部分）

## 讲义与资源

- [B1 讲义](https://ysyx.oscc.cc/docs/2407/b/1.html) | [课件](https://ysyx.oscc.cc/slides/2306/18.html#/) | [视频](https://www.bilibili.com/video/BV1gj411s7ah)
- [B2 讲义](https://ysyx.oscc.cc/docs/2407/b/2.html) | [课件上](https://ysyx.oscc.cc/slides/2306/19.html#/) | [课件下](https://ysyx.oscc.cc/slides/2306/20.html#/) | [视频上](https://www.bilibili.com/video/BV1NC4y1u7K3) | [视频下](https://www.bilibili.com/video/BV1FC4y1k7mP)
- [B3 讲义](https://ysyx.oscc.cc/docs/2407/b/3.html)
- [B4 讲义](https://ysyx.oscc.cc/docs/2407/b/4.html) | [课件](https://ysyx.oscc.cc/slides/2306/21.html#/) | [视频](https://www.bilibili.com/video/BV1xr421F7ZP)
- [B5 讲义](https://ysyx.oscc.cc/docs/2407/b/5.html) | [课件](https://ysyx.oscc.cc/slides/2306/22.html#/) | [视频](https://www.bilibili.com/video/BV1ZRtkeVEqw)
- [B 阶段流片准备与考核](https://ysyx.oscc.cc/docs/2407/2306/basic/1.11.html)
