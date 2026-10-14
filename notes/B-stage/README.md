# B 阶段：SoC 系统设计

把处理器集成为完整系统，是 F 到 B 里时间最长的一段，官方预估 85 小时。B 阶段的结业考核等同于流片考核，通过后拿到 B 级认证和免费流片资格。

## 任务清单

| 序号 | 任务 | 预估 |
|:---:|---|:---:|
| B1 | 总线 | 10h |
| B2 | SoC 计算机系统 | 30h |
| B3 | 时序分析和优化 | 5h |
| B4 | 性能优化和简易缓存 | 20h |
| B5 | 流水线处理器 | 20h |

## 每项在做什么

B1 讲总线：AXI 和 AXI-Lite 这类协议怎么用，互联结构（Crossbar 或者共享总线）怎么选，主设备和从设备之间怎么发起和响应一次传输。

B2 占 30 小时，是这一段时间最长的一项。要把 NPC 处理器接成一个完整的 SoC：挂上 SRAM、ROM、UART、SPI 这些外设，规划地址空间映射，再配一个中断控制器，最后在 FPGA 上运行整个系统。前面各阶段做的都是独立模块，到这一项才集成为一台完整的机器。

B3 是时序分析和优化，5 小时。静态时序分析怎么看、关键路径通常出在哪、时序约束怎么写。

B4 是性能优化和简易缓存，20 小时。Cache 的基本结构、局部性原理、加上缓存之后性能怎么量。这一项的内容和考研 408 里的缓存部分重合。

B5 是把单周期处理器改造成流水线，20 小时。数据冒险和控制冒险各怎么处理（转发还是停顿）、流水线拉起来之后性能怎么算。

## 笔记

还没开始写。

## 代码

SoC 相关的部分也放在 [code/npc/](../../code/npc/) 下。

## 讲义和课件

B1 [讲义](https://ysyx.oscc.cc/docs/2407/b/1.html)｜[课件](https://ysyx.oscc.cc/slides/2306/18.html#/)｜[视频](https://www.bilibili.com/video/BV1gj411s7ah)

B2 [讲义](https://ysyx.oscc.cc/docs/2407/b/2.html)｜[课件上](https://ysyx.oscc.cc/slides/2306/19.html#/)｜[课件下](https://ysyx.oscc.cc/slides/2306/20.html#/)｜[视频上](https://www.bilibili.com/video/BV1NC4y1u7K3)｜[视频下](https://www.bilibili.com/video/BV1FC4y1k7mP)

B3 [讲义](https://ysyx.oscc.cc/docs/2407/b/3.html)

B4 [讲义](https://ysyx.oscc.cc/docs/2407/b/4.html)｜[课件](https://ysyx.oscc.cc/slides/2306/21.html#/)｜[视频](https://www.bilibili.com/video/BV1xr421F7ZP)

B5 [讲义](https://ysyx.oscc.cc/docs/2407/b/5.html)｜[课件](https://ysyx.oscc.cc/slides/2306/22.html#/)｜[视频](https://www.bilibili.com/video/BV1ZRtkeVEqw)

[B 阶段结业考核申请](https://ysyx.oscc.cc/docs/2407/2306/basic/1.11.html)
