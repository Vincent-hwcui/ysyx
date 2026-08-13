# 阶段七：流片 (Tape-out)

## 学习目标

完成芯片的物理设计全流程，从 RTL 综合到 GDSII 生成，最终实现流片。

## 学习内容

- [ ] 集成电路物理设计流程概述
- [ ] 逻辑综合 (Synthesis)
- [ ] 布局规划 (Floorplanning)
- [ ] 布局 (Placement)
- [ ] 时钟树综合 (CTS)
- [ ] 布线 (Routing)
- [ ] 时序分析 (STA)
- [ ] 物理验证（DRC / LVS / ERC）
- [ ] GDSII 生成
- [ ] 封装与测试基础

## 物理设计流程

```
RTL 设计 → 逻辑综合 → 门级网表 → 布局规划 → 布局 → 时钟树综合
                                                      ↓
GDSII ← 物理验证(DRC/LVS) ← 布线 → 时序分析(STA) → 优化
```

## 设计文档

- `physical-design-flow.md` — 物理设计流程笔记
- `synthesis-notes.md` — 综合笔记
- `pnr-notes.md` — 布局布线笔记
- `sta-notes.md` — 时序分析笔记
- `verification-notes.md` — 物理验证笔记
- `tapeout-checklist.md` — 流片检查清单

## 实现进度

- [ ] RTL 综合完成
- [ ] 布局规划完成
- [ ] 布局布线完成
- [ ] 时序分析通过
- [ ] DRC 验证通过
- [ ] LVS 验证通过
- [ ] GDSII 生成
- [ ] 提交流片
- [ ] 收到芯片
- [ ] 芯片功能验证

## 关键参数

> 流片后在此记录关键参数：
> - 工艺节点：
> - 芯片面积：
> - 最高工作频率：
> - 功耗：
> - 晶体管数量：

## 参考资料

- CMOS VLSI Design (Weste & Harris)
- OpenROAD 文档
- 一生一芯流片课程
