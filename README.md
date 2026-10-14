# 一生一芯学习记录

参加"一生一芯"计划（v24.07）的学习记录，从数字逻辑一路做到 RISC-V 处理器、SoC，最后到流片。官方课程主页在 <https://ysyx.oscc.cc/docs/2407/>。

## 这个仓库是什么

主要是给自己留个可追溯的过程。每周做了什么、卡在哪、后来怎么想通的，都写在 `logs/progress.md` 里；画完的电路和写的代码放在 `code/` 下面。笔记写得比较随意，只求以后回头看能想起来当时在纠结什么。

## 现在到哪了

F 阶段进行中，具体在 F3 数字逻辑电路基础（F 阶段官方预估 39 小时，F3 占 20 小时）。

做完了 F1 如何科学地提问、F2 Logisim 的安装和使用、F3.3 用晶体管搭异或门和同或门、F3.4.1 八进制计数法，还有 F3.5 的一串：2-4 译码器（做成了带使能端的 `decoder24` 子电路）、3-8 译码器、4-16 译码器、七段数码管译码器、1-2 译码器，16-4 编码器和 16-4 优先编码器，1 位 2 选 1 和 3 位 4 选 1 选择器，另外还有一个能在十进制和十六进制之间切换的七段数码管。电路都在 `code/logisim/F3-2to4-decoder.circ` 里。

F3.5 还剩加法器和锁存器/触发器，再往后是 F4 计算机系统的状态机模型、F5 支持数列求和的简单处理器、F6 简易输入输出。这些做完才算走进 E 阶段。

## 各阶段大概做什么

| 阶段 | 内容 |
|:---:|---|
| F | 数字逻辑电路、Logisim 里的简单处理器 |
| E | C 语言、硬件描述语言、Linux、RTL 仿真、PA1 |
| D | NEMU 模拟器、AM 运行时、迷你 RISC-V 的 RTL 实现 |
| C | 单周期 NPC、异常处理、RT-Thread |
| B | 总线、SoC、缓存、流水线处理器 |
| A | 虚存管理、特权级和 xv6、启动 Linux |
| S | 官方还没发布 |

E 之后的阶段目录先建好了，内容还没开始写。

## 会用到的工具

Logisim 画数字电路，C 语言写 NEMU 和 AM，Verilog 写 NPC，Verilator 做 RTL 仿真，GTKWave 看波形。指令集按 RV32I / RV32IM / RV32E 往下走，开发环境是 Linux（Ubuntu 22.04）。

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

## 相关文档

学习路线图在 `docs/learning-roadmap.md`，环境搭建在 `docs/environment-setup.md`，讲义/课件/视频的链接汇总在 `docs/resources.md`，git 的日常操作在 `docs/github-guide.md`。

## License

MIT，见 [LICENSE](./LICENSE)。
