# 尔英 ITX i9-12900HK 黑苹果 EFI 引导

[![OpenCore](https://img.shields.io/badge/OpenCore-1.0.5-blue?logo=apple&logoColor=white)](https://github.com/acidanthera/OpenCorePkg)
[![macOS](https://img.shields.io/badge/macOS-Sequoia%2015.6.1-brightgreen?logo=apple&logoColor=white)](https://www.apple.com.cn/macos/)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://GitHub.com/Naereen/StrapDown.js/graphs/commit-activity)

> 🌍 **English Version** → [README_en.md](./README_en.md)

## 📖 项目简介

本仓库提供适用于 **尔英 G660I i9-12900HK ITX主板** 的黑苹果（Hackintosh）OpenCore 引导配置文件，支持 macOS Sequoia 15.6.1 系统，已完整适配 Wi-Fi 和蓝牙功能。

## 🖥️ 硬件配置

| 组件 | 品牌 | 型号 | 规格参数 | 兼容性 |
|:---|:---|:---|:---|:---:|
| **CPU** | Intel | Core i9-12900HK | Alder Lake-H 移动版处理器 | ✅ |
| **内存** | 三星 | DDR4-3200 | 16GB × 2 (32GB 双通道) | ✅ |
| **主存储** | 铠侠 | RC20 | M.2 NVMe PCIe 1TB | ✅ |
| **副存储** | 幻影 | HV2000 Pro | M.2 NVMe PCIe 1TB | ✅ |
| **独显** | AMD | Radeon RX5500XT | 8GB GDDR6 | ✅ |
| **无线网卡** | Intel | AX210 | Wi-Fi 6 + 蓝牙 5.3 (批次006) | ✅ |

## 💻 软件环境

| 组件 | 版本 | 说明 |
|:---|:---|:---|
| **OpenCore** | v1.0.5 | 最新稳定版本 |
| **macOS** | Sequoia 15.6.1 | 已测试稳定运行 |
| **SMBIOS** | MacPro7,1 | 推荐机型标识 |

## ✨ 功能状态

| 功能 | 状态 | 说明 |
|:---|:---:|:---|
| **CPU** | ✅ | 完美支持，包括睿频 |
| **iGPU** | ❌ | 十代以后核显无法驱动 |
| **dGPU** | ✅ | RX5500XT 原生支持 |
| **音频** | ✅ | 音频正常 |
| **有线网络** | ✅ | 2.5G/千兆双以太网卡完美支持 |
| **Wi-Fi** | ✅ | AX210 完美支持 Wi-Fi 6 |
| **蓝牙** | ✅ | 蓝牙 5.3 完美工作 |
| **USB** | ✅ | 所有接口完美适配 |
| **睡眠唤醒** | ✅ | 支持完整的电源管理 |

## 📝 BIOS 设置指南

### 必须禁用的选项
```
Advanced Settings:
├── VT-d                    → Disabled  ⚠️ 必须关闭
├── CFG Lock               → Disabled  🔧 推荐禁用  
└── Secure Boot           → Disabled  🛡️ 必须关闭

Boot Settings:
├── Fast Boot             → Disabled
└── CSM Support          → Disabled
```

## 🚀 使用方法

1. **下载 EFI** - 下载本仓库的完整 EFI 文件夹
2. **BIOS 设置** - 按照上述指南配置 BIOS
3. **制作启动盘** - 使用 balenaEtcher 或类似工具制作 macOS 安装盘
4. **复制 EFI** - 将下载的 EFI 文件夹复制到启动盘的 EFI 分区
5. **安装系统** - 正常安装 macOS Sequoia

## 🔧 后期优化建议

- 使用 [ProperTree](https://github.com/corpnewt/ProperTree) 生成新的序列号
- 根据个人需求调整 OpenCore 配置
- 定期更新 OpenCore 和相关驱动

## 📚 相关资源

- [OpenCore 官方指南](https://dortania.github.io/OpenCore-Install-Guide/)
- [远景论坛](http://bbs.pcbeta.com/) - 技术讨论

## 🤝 贡献指南

欢迎提交 Issues 和 Pull Requests 来改进这个项目！

---

<p align="center">
  <strong>⭐ 如果这个项目对你有帮助，请给个 Star！</strong><br>
  <em>🚀 Powered by OpenCore | 💻 Made with ❤️</em>
</p>


