# 阶段三：RISC-V 指令集架构

## 学习目标

深入理解 RISC-V 指令集，能编写和运行 RISC-V 汇编程序，为 CPU 设计奠定基础。

## 学习内容

- [ ] RISC-V 架构概述与设计哲学
- [ ] RV32I 基本整数指令集（47 条指令）
- [ ] 指令格式（R/I/S/B/U/J 型）
- [ ] 寻址模式
- [ ] 函数调用约定 (Calling Convention) 与栈帧管理
- [ ] 扩展指令集（M 乘法、F/D 浮点、A 原子操作）

## 指令格式速查

| 类型 | 位域分布 | 示例指令 |
|:---:|---------|---------|
| R型 | funct7[31:25] rs2[24:20] rs1[19:15] funct3[14:12] rd[11:7] opcode[6:0] | add, sub, sll |
| I型 | imm[31:20] rs1[19:15] funct3[14:12] rd[11:7] opcode[6:0] | addi, lw, jalr |
| S型 | imm[31:25] rs2[24:20] rs1[19:15] funct3[14:12] imm[11:7] opcode[6:0] | sw, sb, sh |
| B型 | imm[31:25] rs2[24:20] rs1[19:15] funct3[14:12] imm[11:7] opcode[6:0] | beq, bne, blt |
| U型 | imm[31:12] rd[11:7] opcode[6:0] | lui, auipc |
| J型 | imm[31:12] rd[11:7] opcode[6:0] | jal |

## 笔记目录

- `rv32i-overview.md` — RV32I 指令集总览
- `instruction-formats.md` — 指令格式详解
- `calling-convention.md` — 调用约定与栈帧
- `extensions.md` — 扩展指令集笔记
- `assembly-examples.md` — 汇编编程实例

## 实践记录

- [ ] 安装 RISC-V 工具链
- [ ] 编写排序算法汇编程序
- [ ] 编写斐波那契数列汇编程序
- [ ] 使用 Spike 模拟器运行程序
- [ ] 阅读 RISC-V 规范关键章节

## 参考资料

- RISC-V Reader (Patterson & Waterman)
- [RISC-V 规范文档](https://riscv.org/technical/specifications/)
- [RISC-V 汇编入门](https://www.cs.cornell.edu/courses/cs3410/2019sp/guides/isa.html)
