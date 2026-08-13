# 阶段五：CPU 核心设计

## 学习目标

独立设计并实现一个 RISC-V CPU 核心，从单周期到五级流水线，支持冒险处理。

## 学习内容

- [ ] 单周期 CPU 数据通路设计
- [ ] 单周期 CPU 控制器设计
- [ ] 五级流水线（IF / ID / EX / MEM / WB）
- [ ] 数据冒险处理（Forwarding 转发）
- [ ] 控制冒险处理（分支预测、延迟槽）
- [ ] 结构冒险处理
- [ ] 性能分析与优化

## 设计文档

- `single-cycle-design.md` — 单周期 CPU 设计文档
- `pipeline-design.md` — 流水线 CPU 设计文档
- `hazard-handling.md` — 冒险处理方案
- `branch-prediction.md` — 分支预测设计
- `performance-analysis.md` — 性能分析报告

## 实现进度

- [ ] 单周期 CPU — 支持 RV32I 核心子集
- [ ] 单周期 CPU — 支持 RV32I 完整指令集
- [ ] 指令级测试通过
- [ ] 五级流水线改造
- [ ] 数据转发 (Forwarding) 实现
- [ ] Load-Use 冒险停顿 (Stall) 实现
- [ ] 分支预测实现
- [ ] Coremark 性能测试

## 代码位置

- CPU 核心代码: [code/cpu/](../../code/cpu/)
- 仿真测试: [simulation/](../../simulation/)

## 关键设计决策

> 在此记录设计过程中的重要决策和权衡，例如：
> - 选择哪种分支预测策略？为什么？
> - 是否实现延迟槽？为什么？
> - Cache 是否实现？容量和映射方式如何选择？

## 参考资料

- Computer Architecture: A Quantitative Approach (Hennessy & Patterson)
- Computer Organization and Design RISC-V Edition
- 一生一芯课程录播
