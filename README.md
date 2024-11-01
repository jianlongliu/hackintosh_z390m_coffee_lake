# 黑苹果 EFI 配置使用说明

## 项目概述
此项目包含了用于运行 macOS 的黑苹果 EFI 文件，适用于以下硬件配置。

## 系统信息
- **主板型号**: ASRock Z390M Pro4
- **处理器**: Intel i7 9700 (8 核 8 线程)
- **显卡**: AMD Radeon 6950XT
- **内存**: 40GB (DDR4)
- **存储**: SATA SSD / HDD (具体型号视实际情况而定)
- **网络适配器**: Intel I219-V
- **音频芯片**: Realtek ALC892
- **系统版本**: macOS Sequoia

## EFI 文件结构
- `EFI/` 目录：存放 EFI 启动文件
- `OC/` 目录：存放 OpenCore 引导配置文件
- `Drivers/` 目录：存放必要的驱动程序
- `Kexts/` 目录：存放必要的 Kext 文件

## 使用步骤

### 1. 制作启动 U 盘
- 使用 [Rufus](https://rufus.ie/) 制作可启动的 macOS 安装 U 盘。

### 2. 替换 EFI 文件
- 下载或克隆本项目。
- 将 `EFI` 文件夹替换到 U 盘的 `EFI` 目录中。

### 3. BIOS 设置
- 进入 BIOS 设置，确保启用以下选项：
  - CSM（兼容性支持模块）关闭
  - Secure Boot 关闭
  - Fast Boot 关闭
  - 设置 SATA 模式为 AHCI
  - 将 USB 启动设备设置为首选启动项
  - **开启 Above 4G Decoding**（在 BIOS 设置中的 PCIe 配置选项中找到并启用此选项）

### 4. 启动 macOS 安装程序
- 插入 U 盘并重启电脑，选择 U 盘作为启动设备。
- 进入 macOS 安装程序，按照提示进行安装。

### 5. 完成安装
- 安装完成后，重启并进入新的 macOS 系统。
- 在第一次启动时，可能需要再次进入 BIOS 设置，将新安装的系统分区设置为首选启动项。

## 常见问题与解决方案

### 问题 1: 无法启动
- 检查 BIOS 设置是否正确。
- 确保 EFI 文件已正确替换并已正确配置。

### 问题 2: 网络或音频问题
- 确保相关 Kext 文件已正确安装在 `Kexts/` 目录中。

## OpenCore 指南
- 详细的 OpenCore 使用指南请参考 [OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)

## 其他信息
- **OpenCore 版本**: 0.8.8
- **RapidEFI 使用**: 通过 RapidEFI 生成并修补 EFI 文件。

---
ps. README由ChatGPT生成, 我很谢谢它~
