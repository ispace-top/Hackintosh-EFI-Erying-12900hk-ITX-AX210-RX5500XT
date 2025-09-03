# Erying ITX i9-12900HK Hackintosh EFI

[![OpenCore](https://img.shields.io/badge/OpenCore-1.0.5-blue?logo=apple&logoColor=white)](https://github.com/acidanthera/OpenCorePkg)
[![macOS](https://img.shields.io/badge/macOS-Sequoia%2015.6.1-brightgreen?logo=apple&logoColor=white)](https://www.apple.com/macos/)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://GitHub.com/Naereen/StrapDown.js/graphs/commit-activity)

> 🌍 **中文版本** → [README.md](./README.md)

## 📖 Overview

This repository provides a complete OpenCore bootloader configuration for the **Erying G660I i9-12900HK ITX motherboard** to run macOS Sequoia 15.6.1, with full support for Wi-Fi and Bluetooth functionality.

## 🖥️ Hardware Configuration

| Component | Brand | Model | Specifications | Compatibility |
|:---|:---|:---|:---|:---:|
| **CPU** | Intel | Core i9-12900HK | Alder Lake-H Mobile Processor | ✅ |
| **RAM** | Samsung | DDR4-3200 | 16GB × 2 (32GB Dual Channel) | ✅ |
| **Primary Storage** | Kioxia | RC20 | M.2 NVMe PCIe 1TB | ✅ |
| **Secondary Storage** | Phantom | HV2000 Pro | M.2 NVMe PCIe 1TB | ✅ |
| **Discrete GPU** | AMD | Radeon RX5500XT | 8GB GDDR6 | ✅ |
| **Wireless Card** | Intel | AX210 | Wi-Fi 6 + Bluetooth 5.3 (Batch:006) | ✅ |

## 💻 Software Environment

| Component | Version | Note |
|:---|:---|:---|
| **OpenCore** | v1.0.5 | Latest stable release |
| **macOS** | Sequoia 15.6.1 | Tested and stable |
| **SMBIOS** | MacPro7,1 | Recommended system definition |

## ✨ Feature Status

| Feature | Status | Notes |
|:---|:---:|:---|
| **CPU** | ✅ | Perfect support with Turbo Boost |
| **iGPU** | ❌ | No support from the 11th generation. |
| **dGPU** | ✅ | RX5500XT native support |
| **Audio** | ✅ | Audio works perfectly |
| **Ethernet** | ✅ | 2.5G/Gigabit dual Ethernet perfect support |
| **Wi-Fi** | ✅ | AX210 perfect Wi-Fi 6 support |
| **Bluetooth** | ✅ | Bluetooth 5.3 fully working |
| **USB** | ✅ | All ports perfectly mapped |
| **Sleep/Wake** | ✅ | Complete power management support |

## 📝 BIOS Configuration Guide

### Required Disabled Options
```
Advanced Settings:
├── VT-d                    → Disabled  ⚠️ Must disable
├── CFG Lock               → Disabled  🔧 Recommended  
└── Secure Boot           → Disabled  🛡️ Must disable

Boot Settings:
├── Fast Boot             → Disabled
└── CSM Support          → Disabled
```

## 🚀 Installation Guide

1. **Download EFI** - Download the complete EFI folder from this repository
2. **BIOS Setup** - Configure BIOS according to the guide above
3. **Create Installer** - Use balenaEtcher or similar tools to create macOS installer
4. **Copy EFI** - Copy the downloaded EFI folder to the installer's EFI partition
5. **Install System** - Proceed with normal macOS Sequoia installation

## 🔧 Post-Installation Recommendations

- Use [ProperTree](https://github.com/corpnewt/ProperTree) to generate new serial numbers
- Adjust OpenCore configuration based on personal needs
- Keep OpenCore and kexts updated regularly

## 📚 Helpful Resources

- [OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)
- [PCBeta Forum](http://bbs.pcbeta.com/) - Technical discussions

## 🤝 Contributing

Issues and Pull Requests are welcome to improve this project!

---

<p align="center">
  <strong>⭐ If this project helped you, please give it a Star!</strong><br>
  <em>🚀 Powered by OpenCore | 💻 Made with ❤️</em>
</p>
