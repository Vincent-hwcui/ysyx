# One Student One Chip | 一生一芯学习记录

> 记录从零开始学习芯片设计的完整历程，涵盖数字逻辑、计算机体系结构、RISC-V 指令集、CPU 设计、SoC 设计及流片全流程。

## 项目简介

本项目记录本人参加"一生一芯"计划的学习全过程，从数字电路基础到独立完成 RISC-V 处理器设计并流片。通过系统化的学习笔记、代码实现和仿真验证，展示在芯片设计领域的知识积累与实践能力。

## 学习路线

| 阶段 | 内容 | 状态 | 目录 |
|:---:|------|:---:|------|
| 01 | 数字逻辑基础 | 🔲 未开始 | [notes/01-digital-logic](./notes/01-digital-logic) |
| 02 | 计算机组成原理 | 🔲 未开始 | [notes/02-computer-architecture](./notes/02-computer-architecture) |
| 03 | RISC-V 指令集架构 | 🔲 未开始 | [notes/03-risc-v-isa](./notes/03-risc-v-isa) |
| 04 | 硬件描述语言 (Verilog/Chisel) | 🔲 未开始 | [notes/04-hdl-verilog-chisel](./notes/04-hdl-verilog-chisel) |
| 05 | CPU 核心设计 | 🔲 未开始 | [notes/05-cpu-design](./notes/05-cpu-design) |
| 06 | SoC 系统设计 | 🔲 未开始 | [notes/06-soc-design](./notes/06-soc-design) |
| 07 | 流片 (Tape-out) | 🔲 未开始 | [notes/07-tapeout](./notes/07-tapeout) |

> 状态说明: 🔲 未开始 | 🟡 进行中 | ✅ 已完成

## 技术栈

- **指令集架构**: RISC-V (RV32I + 扩展指令)
- **硬件描述语言**: Verilog / Chisel
- **仿真工具**: Verilator / GTKWave / VCS
- **EDA 工具**: Vivado / Design Compiler / Innovus
- **开发板**: Nail (一生一芯指定开发板)
- **其他工具**: Git, Make, Python (测试脚本)

## 仓库结构

```
one-student-one-chip/
├── README.md                  # 项目主页（当前文件）
├── docs/                      # 文档
│   ├── learning-roadmap.md    # 详细学习路线图
│   ├── environment-setup.md   # 开发环境搭建指南
│   └── resources.md           # 学习资源汇总
├── notes/                     # 学习笔记（按阶段组织）
│   ├── 01-digital-logic/      # 数字逻辑基础
│   ├── 02-computer-architecture/  # 计算机组成原理
│   ├── 03-risc-v-isa/         # RISC-V 指令集
│   ├── 04-hdl-verilog-chisel/ # 硬件描述语言
│   ├── 05-cpu-design/         # CPU 设计
│   ├── 06-soc-design/         # SoC 设计
│   └── 07-tapeout/            # 流片
├── code/                      # 代码实现
│   ├── exercises/             # 基础练习
│   ├── cpu/                   # CPU 核心代码
│   └── soc/                   # SoC 代码
├── simulation/                # 仿真验证
│   ├── testbench/             # 测试平台
│   └── waves/                 # 波形截图
├── logs/                      # 学习日志
│   └── progress.md            # 进度记录
├── .gitignore
└── LICENSE
```

## 学习进度

详细进度记录见 [logs/progress.md](./logs/progress.md)。

## 相关文档

- [详细学习路线图](./docs/learning-roadmap.md)
- [开发环境搭建指南](./docs/environment-setup.md)
- [学习资源汇总](./docs/resources.md)

## License

本项目采用 [MIT License](./LICENSE) 开源协议。

---

*此仓库用于记录学习过程，欢迎交流讨论。*
