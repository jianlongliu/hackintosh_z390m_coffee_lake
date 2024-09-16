# 黑苹果 EFI 配置指南

## 硬件信息
- **处理器**: Intel Core i7 9700  
- **内存**: 32GB (ADATA 16GB + Corsair 16GB)  
- **主板**: ASRock Z390M Pro4  
- **显卡**: AMD Radeon 6950XT  
- **硬盘**: Samsung 970 Evo, WDC SN770, Crucial MX500 等

## 先决条件
- **工具**:  
  - [OpenCore](https://github.com/acidanthera/OpenCorePkg)  
  - [RapidEFI](https://github.com/5T33Z0/Rapid-EFI)  
  - Rufus、Python3、OpenCore Configurator

## 安装步骤
1. **创建 macOS 安装器**：使用 `macrecovery.py` 下载 macOS Sonoma 镜像并设置 USB 启动盘。
2. **准备 EFI**：放置驱动（Kext），并根据硬件调整 Quirks。
3. **显卡伪装**：通过 WhateverGreen 和 OpenCore Configurator 将 6950XT 伪装为 6900XT 以兼容 macOS。

## 推荐应用
AltTab、Bartender、iStat Menus、FlClash、Loop、Karabiner Elements 等。

## 鸣谢
基于 OpenCore 官方指南及社区资源整理。

> https://dortania.github.io/OpenCore-Install-Guide/
>
> https://jianlongliu.github.io/posts/1e5fcd72.html
