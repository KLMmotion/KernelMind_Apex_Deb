# KernelMind_Apex_Deb

**KernelMind机械系统和Apex遥操作平台的ARM64 Debian包集合。** 包含机械臂驱动、灵巧手控制和VR遥操作系统的核心依赖库。

[中文](#中文) | [English](#english)

---

## 中文

### 📋 项目概述

本仓库提供KernelMind与Apex遥操作系统的ARM64 Debian包发行版，用于在嵌入式Linux设备（如机械臂控制终端、教育机器人等）上部署完整的遥操作控制栈。包括遥操系统、VR头显驱动、机械臂驱动和灵巧手（舞肌灵巧手）控制库。

### 📦 包含的Deb包

| 包名 | 版本 | 大小 | 架构 | 描述 |
|------|------|------|------|------|
| **Apex-Teleop** | 0.1.0 | 115MB | ARM64 | Apex遥操作系统主程序，支持VR头显、实时视频流和远程控制 |
| **kernelmind-apex** | 1.0.4 | 49MB | ARM64 | KernelMind Apex核心驱动库和运行时环境 |
| **kernelmind-wujihand** | 1.0.3 | 2.3MB | ARM64 | 舞肌灵巧手驱动和控制库 |
| **wujihandcpp** | 1.5.1 | 667KB | ARM64 | 舞肌灵巧手C++开发库和接口 |

### 🚀 快速开始

#### 系统要求
- **架构**: ARM64（aarch64）
- **OS**: Ubuntu 18.04+ / Debian 10+
- **最小存储**: 300MB （所有包总计）

#### 安装步骤

1. **下载所有.deb包**
   ```bash
   git clone https://github.com/hbr853744453-dev/KernelMind_Apex_Deb.git
   cd KernelMind_Apex_Deb
   ```

2. **按顺序安装**（推荐）
   ```bash
   sudo dpkg -i kernelmind-apex_1.0.4_arm64.deb
   sudo dpkg -i wujihandcpp-1.5.1-arm64.deb
   sudo dpkg -i kernelmind-wujihand_1.0.3_arm64.deb
   sudo dpkg -i Apex-Teleop-0.1.0-arm64.deb
   ```

3. **解决依赖问题**（如果有）
   ```bash
   sudo apt-get update
   sudo apt-get install -f
   ```

#### 卸载

```bash
sudo apt-get remove apex-teleop kernelmind-apex kernelmind-wujihand wujihandcpp
```

### ⚙️ 主要功能

- 🎮 **VR遥操控制系统** - 支持VR头显实时控制
- 🦾 **机械臂驱动** - KernelMind Apex机械臂完整驱动栈
- 🖐️ **灵巧手控制** - 舞肌灵巧手多指协调控制库
- 📹 **实时视觉反馈** - 支持远程视频流传输
- 🔧 **C++原生接口** - 便于二次开发

### 🛠️ 故障排查

| 问题 | 解决方案 |
|------|--------|
| `dpkg: dependency problems` | 运行 `sudo apt-get install -f` |
| 架构不兼容 | 确认系统为ARM64: `uname -m` 应显示 `aarch64` |
| 包文件损坏 | 重新下载对应.deb文件 |
| 权限错误 | 使用 `sudo` 运行安装命令 |

### 📚 相关资源

- **发布版本**: 包含VR-meta头显适配版本
- **支持系统**: ARM64 Linux设备
- **开发语言**: C++ / Python

---

## English

### 📋 Project Overview

This repository contains ARM64 Debian packages for KernelMind and Apex teleoperation systems, designed for embedded Linux devices (robotic arm controllers, educational robots, etc.). Includes the complete teleoperation control stack with VR headset drivers, robotic arm drivers, and dexterous hand (Wujimuscle dexterous hand) control libraries.

### 📦 Debian Packages

| Package | Version | Size | Arch | Description |
|---------|---------|------|------|-------------|
| **Apex-Teleop** | 0.1.0 | 115MB | ARM64 | Apex teleoperation system with VR headset support, real-time video streaming and remote control |
| **kernelmind-apex** | 1.0.4 | 49MB | ARM64 | KernelMind Apex core driver and runtime libraries |
| **kernelmind-wujihand** | 1.0.3 | 2.3MB | ARM64 | Wujimuscle dexterous hand driver and control library |
| **wujihandcpp** | 1.5.1 | 667KB | ARM64 | Wujimuscle dexterous hand C++ development library and interfaces |

### 🚀 Quick Start

#### System Requirements
- **Architecture**: ARM64 (aarch64)
- **OS**: Ubuntu 18.04+ / Debian 10+
- **Min Storage**: 300MB (all packages combined)

#### Installation

1. **Clone repository**
   ```bash
   git clone https://github.com/hbr853744453-dev/KernelMind_Apex_Deb.git
   cd KernelMind_Apex_Deb
   ```

2. **Install packages in order** (recommended)
   ```bash
   sudo dpkg -i kernelmind-apex_1.0.4_arm64.deb
   sudo dpkg -i wujihandcpp-1.5.1-arm64.deb
   sudo dpkg -i kernelmind-wujihand_1.0.3_arm64.deb
   sudo dpkg -i Apex-Teleop-0.1.0-arm64.deb
   ```

3. **Resolve dependencies** (if needed)
   ```bash
   sudo apt-get update
   sudo apt-get install -f
   ```

#### Uninstall

```bash
sudo apt-get remove apex-teleop kernelmind-apex kernelmind-wujihand wujihandcpp
```

### ⚙️ Features

- 🎮 **VR Teleoperation System** - Real-time control with VR headset support
- 🦾 **Robotic Arm Drivers** - Complete KernelMind Apex driver stack
- 🖐️ **Dexterous Hand Control** - Multi-fingered Wujimuscle dexterous hand coordination library
- 📹 **Real-time Visual Feedback** - Remote video stream transmission
- 🔧 **Native C++ Interface** - Easy for secondary development

### 🛠️ Troubleshooting

| Issue | Solution |
|-------|----------|
| `dpkg: dependency problems` | Run `sudo apt-get install -f` |
| Incompatible architecture | Verify ARM64 system: `uname -m` should show `aarch64` |
| Corrupted package file | Re-download the .deb file |
| Permission denied | Use `sudo` for installation commands |

### 📚 Resources

- **Releases**: Includes VR-meta headset adapted versions
- **Supported Systems**: ARM64 Linux devices
- **Development Languages**: C++ / Python
# KernelMind_Apex_Deb
