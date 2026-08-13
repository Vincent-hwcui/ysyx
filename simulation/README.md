# 仿真验证目录

此目录存放所有 Testbench 和仿真结果。

## 目录结构

```
simulation/
├── testbench/       # 测试平台
│   ├── tb_alu.v     # ALU 测试
│   ├── tb_cpu.v     # CPU 测试
│   └── ...
├── waves/           # 波形截图
│   ├── alu_wave.png
│   ├── cpu_wave.png
│   └── ...
├── tests/           # 测试程序
│   ├── asm/         # 汇编测试程序
│   └── c/           # C 测试程序
└── scripts/         # 仿真脚本
    ├── run_sim.sh   # 仿真运行脚本
    └── ...
```

## 仿真流程

```bash
# 使用 Verilator 仿真
verilator --cc --exe --build -Wno-fatal tb_module.v module.v sim_main.cpp
./obj_dir/Vmodule

# 使用 Icarus Verilog 仿真
iverilog -o sim_out tb_module.v module.v
vvp sim_out

# 查看波形
gtkwave dump.vcd
```

## 测试策略

1. **模块级测试**: 对每个模块单独编写 Testbench
2. **指令级测试**: 对 CPU 执行的每条指令进行验证
3. **程序级测试**: 运行完整程序验证 CPU 功能
4. **回归测试**: 每次修改后运行全部测试确保不引入回归
