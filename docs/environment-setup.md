# 开发环境搭建指南

> 针对"一生一芯"项目的开发环境配置，涵盖 F~A 阶段所需全部工具。

## 1. 操作系统

推荐使用 **Linux (Ubuntu 22.04 LTS)**。

如使用 Windows，建议：
- **WSL2 + Ubuntu**（推荐）
- Docker 容器
- 双系统

## 2. 基础工具

```bash
sudo apt update && sudo apt upgrade -y

# 基础开发工具
sudo apt install -y build-essential git make gdb python3 python3-pip

# 图形相关（NEMU 需要）
sudo apt install -y libsdl2-dev libreadline-dev

# GTKWave（波形查看器）
sudo apt install -y gtkwave

# 文本处理工具
sudo apt install -y bison flex
```

## 3. RISC-V 工具链

### 3.1 交叉编译工具链

```bash
# 从源码编译
git clone https://github.com/riscv/riscv-gnu-toolchain
cd riscv-gnu-toolchain
./configure --prefix=/opt/riscv --with-arch=rv32im --with-abi=ilp32
make -j$(nproc)
```

### 3.2 验证

```bash
/opt/riscv/bin/riscv32-unknown-elf-gcc --version
```

## 4. 仿真与综合工具

```bash
# Verilator（RTL 仿真）
sudo apt install -y verilator

# Icarus Verilog（备用仿真器）
sudo apt install -y iverilog

# yosys（逻辑综合）
sudo apt install -y yosys
```

## 5. Logisim（F 阶段）

下载 Logisim 图形化数字电路模拟器：
- 官网: <http://www.cburch.com/logisim/>
- 或使用 Logisim-evolution（增强版）

## 6. 获取 ysyx-workbench（一生一芯工作区）

```bash
git clone https://github.com/OSCPU/ysyx-workbench.git
```

工作区包含 NEMU、AM 等子模块，需要初始化子模块：

```bash
cd ysyx-workbench
git submodule update --init
```

## 7. 验证环境

```bash
echo "=== 环境检查 ==="
echo "GCC: $(gcc --version | head -1)"
echo "RISC-V GCC: $(riscv32-unknown-elf-gcc --version | head -1)"
echo "Verilator: $(verilator --version)"
echo "GTKWave: $(gtkwave --version 2>/dev/null || echo 'not found')"
echo "Make: $(make --version | head -1)"
echo "=== 检查完成 ==="
```

## 8. 常见问题

### Q: WSL2 无法显示图形界面？
安装 Windows 的 X Server（VcXsrv/Xming），设置 `DISPLAY` 环境变量。NEMU 的 SDL 图形模式和 GTKWave 需要图形环境。

### Q: NEMU 编译报错缺少 SDL2？
```bash
sudo apt install -y libsdl2-dev libsdl2-2.0-0
```

### Q: 差分测试 (difftest) 需要什么？
需要 NEMU 编译出动态库（`.so`），NPC 通过 DPI-C 接口调用，与 Verilator 配合使用。

### Q: 工具链编译太慢？
`make -j$(nproc)` 用多核加速。零基础建议直接使用官方预编译版本。

---

*更详细的安装问题请参考[官方文档](https://ysyx.oscc.cc/docs/2407/)的对应章节。*
