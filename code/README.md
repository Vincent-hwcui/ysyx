# 代码目录

这里放各阶段实际写的东西。目前只有 F 阶段的 Logisim 电路，后面的 NEMU、AM、NPC 目录先建好了，还没开始写。

## 目录

```
code/
├── logisim/    # F 阶段的 Logisim 电路文件
├── nemu/       # NEMU 指令集模拟器（D 阶段开始）
├── am/         # AM 抽象机器运行时（D 阶段开始）
└── npc/        # NPC 处理器 RTL（D 阶段开始）
```

## logisim/

现在里面是一个文件 `F3-2to4-decoder.circ`，F3 的电路都塞在这一个文件里，用子电路分开：`decoder24`（带使能端的 2-4 译码器）、`decoder38`、`decoder416`、`seg7`（七段数码管译码器）、`decoder12`、`encoder164`、`encoder164p`（优先编码器）、`Multiplexer121`、`Multiplexer341`、`seg7switch`（能切换十进制和十六进制的七段数码管）、`HalfAdder` 和 `FullAdder`、`YuanMaAdder4bit`（原码加法器）、`FanMaAdder4bit`（反码加法器）、`Adder4bitOverflowJudge`（带溢出判断的补码加法器）。时序部分有 `SRLatch`、`DLatch`、`DLatchReset`、`DFlipFlop`、`DFlipFlopReset`、`DFlipFlopEnReset`、`Register4Bit`、`Counter4Bit`、`Sum1to10`（数列求和），以及电子时钟的 `Digit9`、`Digit5`、`EClock`。

做成一个文件是因为 Logisim 的子电路可以互相调用，比如 `decoder38` 里直接放了两个 `decoder24` 实例，改公共部分的时候不用两边同步。

## nemu/、am/、npc/

等做到 D 阶段再动。NEMU 是 C 写的指令集模拟器，后面所有处理器的正确性都靠跟它做差分测试来验证；AM 是一层薄薄的运行时，让同一份程序既能跑在 NEMU 上也能跑在自己的处理器上；NPC 是用 Verilog 写的处理器，从单周期一路做到流水线，最后集成进 SoC。
