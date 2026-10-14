# 学习资源汇总

主要用官方 v24.07 的资源，另外记了几个会用到的开源项目和教材。

## 官方入口

课程主页在 <https://ysyx.oscc.cc/docs/2407/>，B 站直播在 <https://live.bilibili.com/24416626>，录播在 <https://space.bilibili.com/2107852263/lists/6324990>。

每个任务对应的讲义、课件、视频链接，我在各阶段的 README 里都列了一份，直接看那里比较方便：F 阶段在 [notes/F-preliminary/](../notes/F-preliminary/)，E 阶段在 [notes/E-entry/](../notes/E-entry/)，D 在 [notes/D-stage/](../notes/D-stage/)，C 在 [notes/C-stage/](../notes/C-stage/)，B 在 [notes/B-stage/](../notes/B-stage/)。A 阶段的讲义官方还没发布，S 阶段还标着"待续"。

## 会读到的开源项目

NEMU（指令集模拟器）在 [NJU-ProjectN/nemu](https://github.com/NJU-ProjectN/nemu)，AM（抽象机器运行时）在 [NJU-ProjectN/abstract-machine](https://github.com/NJU-ProjectN/abstract-machine)，官方的工作区模板在 [OSCPU/ysyx-workbench](https://github.com/OSCPU/ysyx-workbench)。这三个仓库的代码都要读，特别是 NEMU，后面验证处理器要拿它当参考。

## 教材

除了讲义，另外找了几本对着看：袁春风的《计算机系统基础》（南大 ICS 的教材），Harris 的《Digital Design and Computer Architecture》，Patterson 和 Hennessy 的《Computer Organization and Design》RISC-V 版，还有 Patterson 的《RISC-V Reader》。数字电路那部分 F3 卡住的时候，Harris 那本讲得比讲义细。

## 工具

Logisim 的官网是 <http://www.cburch.com/logisim/>，Verilator 的文档在 <https://verilator.org/guide/latest/>，GTKWave 在 <http://gtkwave.sourceforge.net/>。RISC-V 的规范在 <https://riscv.org/technical/specifications/>，查指令编码的时候用得上。
