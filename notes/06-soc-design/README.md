# 阶段六：SoC 系统设计

## 学习目标

将 CPU 核心集成到完整的 SoC 系统中，实现总线通信和外设接口。

## 学习内容

- [ ] SoC 顶层架构设计
- [ ] 总线协议（AXI / APB / AHB / 自定义总线）
- [ ] 地址空间映射
- [ ] 外设接口设计
  - [ ] UART 串口
  - [ ] SPI 接口
  - [ ] GPIO
  - [ ] Timer / PWM
- [ ] 中断系统（PLIC / CLINT）
- [ ] 存储系统（SRAM / ROM / Flash 接口）
- [ ] DMA 控制器

## 设计文档

- `soc-architecture.md` — SoC 架构设计
- `address-map.md` — 地址空间映射表
- `bus-protocol.md` — 总线协议设计
- `peripherals.md` — 外设接口设计
- `interrupt-system.md` — 中断系统设计

## 实现进度

- [ ] SoC 顶层模块搭建
- [ ] 总线互联 (Bus Interconnect)
- [ ] UART 串口通信实现
- [ ] SPI 接口实现
- [ ] GPIO 实现
- [ ] Timer 实现
- [ ] 中断控制器实现
- [ ] FPGA 上板验证

## SoC 地址空间映射（示例）

| 外设 | 基地址 | 大小 | 说明 |
|------|--------|------|------|
| ROM | 0x0000_0000 | 64KB | Boot ROM |
| SRAM | 0x0200_0000 | 256KB | 片上 SRAM |
| UART | 0x1000_0000 | 4KB | 串口 |
| SPI | 0x1000_1000 | 4KB | SPI 控制器 |
| GPIO | 0x1001_0000 | 4KB | GPIO |
| CLINT | 0x0200_0000 | 4KB | 核心本地中断 |
| PLIC | 0x0C00_0000 | 64KB | 平台级中断 |

## 代码位置

- SoC 代码: [code/soc/](../../code/soc/)
- 仿真测试: [simulation/](../../simulation/)

## 参考资料

- RISC-V Privileged ISA Specification
- AMBA AXI/APB Protocol Specification
- 一生一芯 SoC 设计课程
