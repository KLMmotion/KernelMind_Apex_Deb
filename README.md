# KernelMind_Apex_Deb

**KernelMind 遥操系统与 Apex 遥操作平台 ARM64 Debian 包集合**

> 本仓库收录了 KernelMind 舞肌灵巧手机器手控制及 VR 遥操作核心软件的 ARM64 Debian (.deb) 安装包，方便在机器人、教育、科研等场景中一键部署全部运行环境。

[中文](#中文) | [English](#english)

---

## 中文

### 📝 项目简介

- 提供 KernelMind 机械臂 + 舞肌灵巧手的核心驱动和遥操作控制系统。
- 支持 VR 头显人机交互、实时远程视频与二次开发。
- 针对 ARM64 架构嵌入式 Linux 设备（如 NVIDIA Jetson、瑞芯微机器人控制终端）优化。

### 📦 已含主要 Deb 包

| 包名                  | 版本   | 架构 | 描述                     |
|---------------------|-------|------|------------------------|
| apex-teleop         | 0.1.0 | ARM64| VR遥操作系统上位机主程序，实时视频流、远程遥控 |
| kernelmind-apex     | 1.0.4 | ARM64| KernelMind Apex 遥操系统 |
| kernelmind-wujihand | 1.0.3 | ARM64| 舞肌灵巧手驱动与控制库     |
| wujihandcpp         | 1.5.1 | ARM64| 舞肌灵巧手 C++ 开发接口    |

### 🚀 安装说明

#### 系统环境要求

- **架构**: ARM64 (aarch64)
- **系统**: Ubuntu 18.04+/Debian 10+
- **存储**: 至少 300MB

#### 步骤

1. 克隆仓库
   ```bash
   git clone https://github.com/KLMmotion/KernelMind_Apex_Deb.git
   cd KernelMind_Apex_Deb
   ```

2. 按顺序安装 `.deb` 包（推荐）
   ```bash
   sudo dpkg -i kernelmind-apex_1.0.4_arm64.deb
   sudo dpkg -i wujihandcpp-1.5.1-arm64.deb
   sudo dpkg -i kernelmind-wujihand_1.0.3_arm64.deb
   sudo dpkg -i Apex-Teleop-0.1.0-arm64.deb
   ```

3. 自动修复依赖（如有）
   ```bash
   sudo apt-get update
   sudo apt-get install -f
   ```

#### 卸载

```bash
sudo apt-get remove apex-teleop kernelmind-apex kernelmind-wujihand wujihandcpp
```

### ⚙️ 功能亮点

- 🎮 支持 VR 头显（如 Pico、Meta）遥控机械臂与灵巧手
- 🦾 提供完整机械臂控制驱动栈
- 🖐️ 多指灵巧手协调控制
- 📹 实时视觉/视频流返回
- 🧰 C++/Python 二次开发友好接口

### 🚦 常见问题排查

| 问题                     | 解决方法                      |
|------------------------|-----------------------------|
| dpkg: dependency problems | 运行 `sudo apt-get install -f` |
| 系统架构不兼容             | 用 `uname -m` 检查, 必须为 `aarch64`|
| 安装包损坏                | 重新下载相应 .deb 文件         |
| 权限错误                  | 装包命令加 `sudo`            |

### 🔗 相关信息

- **支持系统**: ARM64 Linux
- **开发语言**: C++/Python（仓库为二进制发行, 如需源码请联系项目方）
- **应用场景**: 机器人本体控制、远程 VR 遥操作、教育科研

---

## English

### 📝 Overview

- Debian packages for KernelMind robotic systems and Apex VR teleoperation, targeting ARM64 Linux (NVIDIA Jetson, industrial robot controllers, etc).
- Includes core drivers for robotic arms, dexterous hands, and VR-based remote operation.
- Supports VR headset operation, real-time video streaming, and secondary development.

### 📦 Included Packages

| Package               | Version | Arch | Description                                            |
|-----------------------|---------|------|--------------------------------------------------------|
| apex-teleop           | 0.1.0   | ARM64| VR teleop system, real-time streaming & remote control |
| kernelmind-apex       | 1.0.4   | ARM64| KernelMind Apex robot arm driver, runtime libraries    |
| kernelmind-wujihand   | 1.0.3   | ARM64| Wujimuscle dexterous hand driver & control library     |
| wujihandcpp           | 1.5.1   | ARM64| Wujimuscle C++ dev interface for dexterous hand        |

### 🚀 Quick Start

#### Requirements

- **Arch**: ARM64 (aarch64)
- **OS**: Ubuntu 18.04+/Debian 10+
- **Storage**: ≥ 300MB

#### Steps

1. Clone repo
   ```bash
   git clone https://github.com/KLMmotion/KernelMind_Apex_Deb.git
   cd KernelMind_Apex_Deb
   ```
2. Install packages in order (recommended)
   ```bash
   sudo dpkg -i kernelmind-apex_1.0.4_arm64.deb
   sudo dpkg -i wujihandcpp-1.5.1-arm64.deb
   sudo dpkg -i kernelmind-wujihand_1.0.3_arm64.deb
   sudo dpkg -i Apex-Teleop-0.1.0-arm64.deb
   ```
3. Resolve dependencies (if needed)
   ```bash
   sudo apt-get update
   sudo apt-get install -f
   ```

#### Uninstall

```bash
sudo apt-get remove apex-teleop kernelmind-apex kernelmind-wujihand wujihandcpp
```

### ⚙️ Features

- 🎮 VR headset support for real-time teleoperation
- 🦾 Full robot arm driver stack
- 🖐️ Multi-finger dexterous hand control
- 📹 Real-time video streaming feedback
- 🧰 C++/Python developer interfaces

### 🚦 Troubleshooting

| Issue                       | Solution                            |
|-----------------------------|-------------------------------------|
| dpkg: dependency problems   | Run `sudo apt-get install -f`       |
| Incompatible architecture   | Use `uname -m`; must be `aarch64`   |
| Package file corrupted      | Re-download the corresponding .deb   |
| Permission denied           | Prepend `sudo` to install commands  |

### 🔗 Info

- **Supported OS**: ARM64 Linux
- **Languages**: C++/Python (distribution is binary releases; contact us for sources)
- **Use Cases**: Robotics, VR teleoperation, Education, R&D

---

> **如需详细功能描述、版本变更历史或SDK文档，请联系 KernelMind 官方团队！**
