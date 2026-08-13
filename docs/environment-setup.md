# 开发环境搭建指南

## 1. 操作系统

推荐使用 **Linux (Ubuntu 22.04 LTS)** 作为主要开发环境。

如使用 Windows，建议通过以下方式之一：
- **WSL2 + Ubuntu** (推荐)
- **双系统安装 Ubuntu**
- **Docker 容器**

## 2. 基础工具安装

```bash
# 更新系统
sudo apt update && sudo apt upgrade -y

# 安装基础开发工具
sudo apt install -y build-essential git make python3 python3-pip

# 安装 GTKWave（波形查看器）
sudo apt install -y gtkwave
```

## 3. RISC-V 工具链

### 3.1 安装 RISC-V GCC 交叉编译工具链

```bash
# 方法一：从源码编译（推荐，可自定义）
git clone https://github.com/riscv/riscv-gnu-toolchain
cd riscv-gnu-toolchain
./configure --prefix=/opt/riscv
make -j$(nproc)

# 方法二：直接安装预编译版本
sudo apt install -y gcc-riscv64-unknown-elf
```

### 3.2 验证安装

```bash
riscv64-unknown-elf-gcc --version
```

## 4. 仿真工具

### 4.1 Verilator

```bash
# 安装 Verilator
sudo apt install -y verilator

# 验证
verilator --version
```

### 4.2 Icarus Verilog (备用)

```bash
sudo apt install -y iverilog
```

## 5. Chisel 开发环境 (如使用 Chisel)

### 5.1 安装 Java JDK

```bash
sudo apt install -y openjdk-17-jdk
```

### 5.2 安装 sbt

```bash
echo "deb https://repo.scala-sbt.org/scalasbt/debian all main" | sudo tee /etc/apt/sources.list.d/sbt.list
echo "deb https://repo.scala-sbt.org/scalasbt/debian /" | sudo tee /etc/apt/sources.list.d/sbt_old.list
curl -sL "https://keyserver.ubuntu.com/pks/lookup?op=get&search=0x2EE0EA64E40A89B84B2DF73499E82A75642AC823" | sudo apt-key add -
sudo apt update
sudo apt install -y sbt
```

## 6. EDA 工具

### 6.1 Vivado (FPGA 开发)

- 从 AMD/Xilinx 官网下载 Vivado Design Suite
- 推荐安装 Vivado ML Edition (免费版即可)

### 6.2 开源 EDA 工具 (用于流片物理设计)

```bash
# OpenROAD (开源物理设计流程)
sudo apt install -y openroad

# yosys (开源综合工具)
sudo apt install -y yosys

# magic (版图编辑器)
sudo apt install -y magic

# netgen (LVS 验证)
sudo apt install -y netgen
```

## 7. Spike 模拟器 (RISC-V ISA Simulator)

```bash
git clone https://github.com/riscv-software-src/riscv-isa-sim
cd riscv-isa-sim
mkdir build && cd build
../configure --prefix=/opt/riscv
make -j$(nproc)
sudo make install
```

## 8. Git 配置

```bash
# 配置用户名和邮箱
git config --global user.name "你的名字"
git config --global user.email "你的邮箱"

# 配置默认分支名
git config --global init.defaultBranch main
```

## 9. 验证环境

运行以下命令确认所有工具已正确安装：

```bash
echo "=== 环境检查 ==="
echo "GCC: $(gcc --version | head -1)"
echo "RISC-V GCC: $(riscv64-unknown-elf-gcc --version | head -1)"
echo "Verilator: $(verilator --version)"
echo "GTKWave: $(gtkwave --version 2>/dev/null || echo 'not found')"
echo "Git: $(git --version)"
echo "Python: $(python3 --version)"
echo "=== 检查完成 ==="
```

## 10. 常见问题

### Q: WSL2 中无法使用 GTKWave 图形界面？

确保 Windows 上安装了 X Server（如 VcXsrv 或 Xming），并设置 `DISPLAY` 环境变量。

### Q: RISC-V 工具链编译时间太长？

使用 `make -j$(nproc)` 利用多核加速，或在[预编译版本页面](https://github.com/riscv-software-src/riscv-gnu-toolchain/releases)下载。

### Q: Chisel 编译速度慢？

sbt 首次编译需要下载大量依赖，后续编译会使用缓存。可以配置 sbt 的国内镜像加速。
