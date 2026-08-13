# One Student One Chip | 一生一芯学习记录

> 记录本人参加"一生一芯"（v24.07）课程的学习历程，从数字逻辑到 RISC-V 处理器设计、SoC 集成直至流片的完整过程。
>
> 官方课程主页: <https://ysyx.oscc.cc/docs/2407/>

## 项目简介

本项目记录本人参加"一生一芯"计划的学习全过程。通过系统化的学习笔记、代码实现（NEMU / AM / NPC）和仿真验证，展示在处理器设计与芯片设计领域的知识积累与实践能力。

## 学习阶段

| 阶段 | 名称 | 核心内容 | 状态 |
|:---:|------|---------|:---:|
| **F** | 前置学习 | 数字逻辑、Logisim 处理器 | 🔲 |
| **E** | 入门学习 | C语言、HDL、Linux、RTL 仿真、PA1 | 🔲 |
| **D** | 正式学习 | NEMU、AM、迷你 RISC-V RTL | 🔲 |
| **C** | 处理器实现 | 单周期 NPC、异常处理、RT-Thread | 🔲 |
| **B** | SoC 系统 | 总线、SoC、缓存、流水线 | 🔲 |
| **A** | 进阶学习 | 虚存、特权级、xv6、Linux | 🔲 |
| **S** | 高阶挑战 | 待官方发布 | 🔲 |

> 状态说明: 🔲 未开始 | 🟡 进行中 | ✅ 已完成

## 技术栈与核心工具

| 工具 | 类型 | 作用 |
|------|------|------|
| **NEMU** | C 语言模拟器 | 指令集模拟器，差分测试参考实现 |
| **AM** | 运行时库 | 抽象机器，硬件抽象层 |
| **NPC** | Verilog RTL | RISC-V 处理器实现 |
| **Logisim** | 图形化电路 | 数字电路设计（F 阶段） |
| **Verilator** | 仿真工具 | RTL 仿真 |
| **GTKWave** | 波形查看 | 调试波形 |

- **指令集架构**: RISC-V (RV32I / RV32IM / RV32E)
- **硬件描述语言**: Verilog
- **开发环境**: Linux (Ubuntu 22.04)

## 仓库结构

```
one-student-one-chip/
├── README.md                  # 项目主页（当前文件）
├── docs/                      # 文档
│   ├── learning-roadmap.md    # 学习路线图（官方 F~S 阶段）
│   ├── environment-setup.md   # 开发环境搭建指南
│   ├── resources.md           # 官方讲义/课件/视频链接汇总
│   └── github-guide.md        # GitHub 仓库创建与推送指南
├── notes/                     # 学习笔记（按官方阶段组织）
│   ├── F-preliminary/         # F 前置学习
│   ├── E-entry/               # E 入门学习
│   ├── D-stage/               # D 正式学习
│   ├── C-stage/               # C 处理器实现
│   ├── B-stage/               # B SoC 系统
│   ├── A-stage/               # A 进阶学习
│   └── S-stage/               # S 高阶挑战
├── code/                      # 代码实现
│   ├── logisim/               # Logisim 电路文件
│   ├── nemu/                  # NEMU 模拟器
│   ├── am/                    # AM 抽象机器
│   └── npc/                   # NPC 处理器
├── simulation/                # 仿真验证
│   ├── testbench/             # 测试平台
│   └── waves/                 # 波形截图
├── logs/
│   └── progress.md            # 学习进度日志
├── .gitignore
└── LICENSE
```

## 学习进度

详细进度记录见 [logs/progress.md](./logs/progress.md)。

## 相关文档

- [详细学习路线图](./docs/learning-roadmap.md)
- [开发环境搭建指南](./docs/environment-setup.md)
- [学习资源汇总](./docs/resources.md)
- [GitHub 仓库创建与推送指南](./docs/github-guide.md)

## License

本项目采用 [MIT License](./LICENSE) 开源协议。

---

*此仓库用于记录学习过程，欢迎交流讨论。*
