# 仿真验证目录

此目录存放 Testbench 和仿真结果。

## 目录结构

```
simulation/
├── testbench/       # 测试平台
│   ├── tb_alu.v     # ALU 测试
│   ├── tb_npc.v     # NPC 处理器测试
│   └── ...
└── waves/           # 波形截图
    ├── alu_wave.png
    ├── npc_wave.png
    └── ...
```

## 仿真与差分测试

"一生一芯"项目的核心验证方法是**差分测试（difftest）**：

```
            ┌─────────────┐
            │  NEMU 模拟器 │  ← 参考实现（软件）
            └──────┬──────┘
                   │ 对比
            ┌──────┴──────┐
            │  NPC 处理器  │  ← 待验证实现（RTL）
            └─────────────┘
```

NPC 每执行一条指令，都与 NEMU 的状态（寄存器、PC、内存）对比，确保 RTL 实现与指令集语义一致。

## 常用仿真命令

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
2. **差分测试**: NPC 与 NEMU 逐指令对比
3. **程序级测试**: 运行完整程序（如跑 RT-Thread、xv6）
4. **回归测试**: 每次修改后运行全部测试
