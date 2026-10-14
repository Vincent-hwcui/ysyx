# 开发环境搭建

这一段还没真正动手，先把想到的记下来，等做 E3 的时候再补实际踩过的坑。

## 现在的情况

日常在 Windows 上，F 阶段用的 Logisim 是图形界面软件，直接跑没问题。麻烦在后面：NEMU、AM、RISC-V 工具链、Verilator 这一串基本都在 Linux 下用，官方也是按 Ubuntu 22.04 写的讲义。

本来想走 WSL2，但**这台机器上 WSL 被安全策略挡住了，起不来**，所以要么开个虚拟机装 Ubuntu，要么找台 Linux 机器。这件事先记着，等 F 阶段收尾之前解决掉，别拖到 E 阶段卡壳。

## 到时候需要装的东西

分四块。基础工具是编译器和调试那一套（gcc、make、gdb、python3），NEMU 还需要 SDL2 和 readline 的库来支持图形和命令行交互。第二块是 RISC-V 交叉编译工具链，官方的做法是从源码编，参数按 rv32im/ilp32 来配，编完用 `riscv32-unknown-elf-gcc --version` 验一下。第三块是仿真和综合：Verilator 用来跑 RTL 仿真，GTKWave 看波形，yosys 做逻辑综合。第四块是官方的工作区 ysyx-workbench，clone 下来之后记得 `git submodule update --init` 把 NEMU 和 AM 这些子模块拉全。

## 暂时不确定的

WSL 那条路走不通的情况下，虚拟机里跑 Verilator 和 GTKWave 卡不卡、需不需要配图形界面转发，这些等真装的时候再试。官方的文档里有一节专门讲环境问题，遇到报错先去那里对一遍。
