# 阶段四：硬件描述语言 (Verilog/Chisel)

## 学习目标

熟练使用 Verilog 或 Chisel 进行硬件描述和建模，能编写 Testbench 进行仿真验证。

## 学习内容

### Verilog 路线
- [ ] 模块定义与端口声明
- [ ] 数据类型（wire, reg, logic）
- [ ] 组合逻辑建模（assign, always @(*)）
- [ ] 时序逻辑建模（always @(posedge clk)）
- [ ] Testbench 编写
- [ ] 参数化设计

### Chisel 路线（可选）
- [ ] Scala 基础语法
- [ ] Chisel 模块定义
- [ ] 组合逻辑与时序逻辑
- [ ] Chisel Testers

## 笔记目录

- `verilog-basics.md` — Verilog 基础语法
- `combinational-modeling.md` — 组合逻辑建模
- `sequential-modeling.md` — 时序逻辑建模
- `testbench.md` — Testbench 编写指南
- `chisel-basics.md` — Chisel 基础（如使用）

## 实践记录

- [ ] 实现 ALU (算术逻辑单元)
- [ ] 实现寄存器堆 (Register File)
- [ ] 实现存储器模型 (SRAM)
- [ ] 编写 Testbench 并使用 GTKWave 查看波形
- [ ] HDLBits 全部练习完成

## 代码位置

- 基础练习代码: [code/exercises/](../../code/exercises/)

## 参考资料

- [HDLBits 在线练习](https://hdlbits.01xz.net/) (强烈推荐)
- Digital Design and Computer Architecture (Harris & Harris) Verilog 章节
- [Verilator 文档](https://verilator.org/guide/latest/)
