# 一生一芯学习记录

"一生一芯"计划的练习记录，跟的是 v24.07 版课程。官方课程主页：<https://ysyx.oscc.cc/docs/2407/>

## 内容

`code/` 放各阶段的代码和电路，`notes/` 放按阶段分的笔记，`logs/progress.md` 记录每周的进度和踩过的坑，`docs/` 放路线图、环境搭建、资源链接和 git 操作备忘。

## 进度

F 阶段进行中，F3 已完成，正在做 F5 支持数列求和的简单处理器。

已完成：F1 如何科学地提问、F2 Logisim 安装和使用、F3.3 用晶体管搭异或门和同或门、F3.4.1 八进制计数法，F3.5 里的 2-4 译码器、3-8 译码器、4-16 译码器、七段数码管译码器、1-2 译码器、16-4 编码器、16-4 优先编码器、1 位 2 选 1 选择器、3 位 4 选 1 选择器、可切换进制的七段数码管，以及加法器、减法器、原码/反码/补码加法器和溢出的检测。F3 的时序逻辑也做完了，从 SR 锁存器、D 锁存器、D 触发器一路做到 4 位寄存器、4 位计数器、数列求和和电子时钟。F4 计算机系统的状态机模型这一章也看完了，内容包括把处理器看成状态机、编译和 CPU 设计在状态机模型下的关系、指令集和处理器属于不同层次。F5 做到了数据通路的前三块：用多路选择器实现的 8字×8位 ROM、4字×8位的寄存器堆 GPR、以及只支持 li 指令的 sCPU，能按 PC 从 ROM 取指令、拆出 rd 和 imm 写回寄存器。电路都在 `code/logisim/F3-2to4-decoder.circ`。

未完成：F3 里只剩与非门版 SR 锁存器的分析和下降沿触发的 D 触发器；F5 还差 add 和 bner0 两条指令的译码、ALU 和跳转逻辑；之后是 F6 功能完备的迷你 RISC-V 处理器。E 阶段及以后没有开始。

## 各阶段

| 阶段 | 内容 | 官方预估 |
|:---:|---|---:|
| F | 数字逻辑电路、Logisim 处理器 | 39h |
| E | C 语言、硬件描述语言、Linux、RTL 仿真、PA1 | 100h |
| D | NEMU 模拟器、AM 运行时、迷你 RISC-V 的 RTL 实现 | 34h |
| C | 单周期 NPC、异常处理、RT-Thread | 29h |
| B | 总线、SoC、缓存、流水线处理器 | 85h |
| A | 虚存管理、特权级和 xv6、启动 Linux | 未定 |
| S | 未发布 | — |

时间是官方按中等水平给的预估，零基础要 2~3 倍。

## 工具

Logisim（F 阶段）、C（NEMU、AM）、Verilog（NPC）、Verilator、GTKWave。指令集为 RV32I / RV32IM / RV32E，环境 Ubuntu 22.04。

## 目录

```
ysyx/
├── README.md
├── docs/                      # 文档
│   ├── learning-roadmap.md    # 学习路线图
│   ├── environment-setup.md   # 开发环境搭建
│   ├── resources.md           # 讲义/课件/视频链接汇总
│   └── github-guide.md        # git 日常操作
├── notes/                     # 学习笔记，按 F~S 阶段分目录
│   ├── F-preliminary/
│   ├── E-entry/
│   ├── D-stage/
│   ├── C-stage/
│   ├── B-stage/
│   ├── A-stage/
│   └── S-stage/
├── code/
│   ├── logisim/               # Logisim 电路
│   ├── nemu/                  # NEMU 模拟器
│   ├── am/                    # AM 抽象机器
│   └── npc/                   # NPC 处理器
├── simulation/                # 仿真验证（测试平台、波形）
├── logs/
│   └── progress.md            # 学习进度日志
├── .gitignore
└── LICENSE
```

## 其他文档

学习路线图 `docs/learning-roadmap.md`，环境搭建 `docs/environment-setup.md`，资源链接 `docs/resources.md`，git 操作 `docs/github-guide.md`。

## License

MIT，见 [LICENSE](./LICENSE)。
