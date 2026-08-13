# 代码目录

此目录存放所有 Verilog/Chisel 代码实现。

## 目录结构

```
code/
├── exercises/       # 基础练习代码
│   ├── alu.v        # ALU 实现
│   ├── regfile.v    # 寄存器堆
│   └── ...
├── cpu/             # CPU 核心代码
│   ├── single-cycle/  # 单周期 CPU
│   ├── pipeline/      # 流水线 CPU
│   └── ...
└── soc/             # SoC 系统代码
    ├── top/           # SoC 顶层
    ├── uart/          # UART 模块
    ├── spi/           # SPI 模块
    └── ...
```

## 编码规范

- 模块名使用小写字母和下划线（如 `alu_module`）
- 端口名使用小写字母和下划线
- 使用有意义的信号名，避免单字母命名（循环变量除外）
- 每个模块文件头部添加注释说明模块功能
- 关键逻辑添加注释

## 代码模板

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
