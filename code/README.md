# 代码目录

此目录存放"一生一芯"项目相关的所有代码实现。

## 目录结构

```
code/
├── logisim/        # F 阶段：Logisim 数字电路文件
│   ├── F3/         # 数字逻辑电路
│   ├── F5/         # 简单处理器
│   └── F6/         # 迷你 RISC-V 处理器
├── nemu/           # NEMU (NJU Emulator) 指令集模拟器
├── am/             # AM (Abstract Machine) 抽象机器运行时
└── npc/            # NPC (New Processor Core) RISC-V 处理器 RTL 实现
```

## 三大核心项目

### NEMU — 指令集模拟器
- C 语言实现的全系统模拟器
- 支持 RV32IM 等指令集
- 作为差分测试（difftest）的参考实现

### AM — 抽象机器运行时
- 硬件抽象层（HAL）
- 让程序在不同机器上统一运行
- 提供 TRM（Turing Machine）、IOE（IO Extension）等模块

### NPC — RISC-V 处理器
- Verilog/Chisel 实现的 RISC-V 处理器
- 从单周期到流水线
- 最终集成到 SoC 并流片

## 编码规范

- 模块名使用小写字母和下划线（如 `alu_module`）
- 使用有意义的信号名，避免单字母命名（循环变量除外）
- 每个模块文件头部添加注释说明模块功能
- 关键逻辑添加注释

## Verilog 代码模板

```verilog
// module_name.v
// 功能描述：简述模块功能
// 作者：[你的名字]
// 日期：YYYY-MM-DD

module module_name (
    input  wire        clk,
    input  wire        rst_n,
    // 输入端口
    // 输出端口
);

    // 内部信号声明

    // 逻辑实现

endmodule
```
