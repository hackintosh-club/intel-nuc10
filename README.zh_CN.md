
## Intel NUC10 黑苹果 OpenCore EFI

### [English](README.md)

### OpenCore

[OpenCore 0.8.4](https://github.com/acidanthera/OpenCorePkg)


### 适配机型

- NUC10i7FNH/FNK
- NUC10i5FNH/FNK
- NUC10i3FNH/FNK


### 可安装系统

- macOS Monterey 12.x (Default `config.plist`)
- macOS Big Sur 11.6.x (Replace `config.plist` with `config.BigSur.plist`)
- macOS Catalina 10.15.x (Replace `config.plist` with `config.Catalina.plist`)


### BIOS 设置

**最新版本（0055以后）升级后会导致 `CFGLock.efi` 失效!!!** 

**怎样升级到最新版本 `0058`** 
1. 在0055版本上解锁 `CFGLock`, 保证 `CFG Lock` 值为 `0`
2. 升级BIOS至最新版本 `0058`
3. 进入 `CFGLock` , 查看 `CFG Lock` 值是否为 `0`, 为 `0` 则可以正常使用.


BIOS version **FNCML357.0058(CFG Unlocked under 0055)**

+ Advanced
  - Storage
    * SATA Mode Selection -> AHCI
  - Video
    * IGD Minimum Memory -> 64MB
    * IGD Aperture Size -> 256MB
    * IGD Primary Video Port -> Auto
+ Boot 
  - Secure Boot
    * Secure Boot -> Disabled
  - Boot Priority
    * UEFI Boot -> Checked
    * Legacy Boot -> Unchecked
    * Fast Boot -> Unchecked
+ Power
  - Secondary Power Settings
    * Deep S4/S5 -> On
    * Wake on Lan from S4/S5 -> Stay Off
    * Wake System from S5 -> Off
    * Wake From Thunderbolt Device -> Off

其它默认设置即可。


### CFG Unlock

新机器或之前未安装过 macOS 的机器，需要解锁CFGLock，具体步骤如下：

1. 找一个U盘，格式化为 `FAT32` 分区。
2. 下载 `EFI` 文件，解压放到U盘根目录。（注意：目录结构应为`/EFI`）。
3. 将U盘插入NUC，重启，按`F10`，选择从刚才放入 `EFI` 文件的那个U盘启动。 
4. 选择 `CFGLock Shell.efi` 选择回车，进行解锁。

注意：若在OC引导界面看不到 `CFGLock Shell.efi` ，按`空格键`即可显示。


**在 OC 引导界面，按 `空格键` 可显示辅助功能**


### 已知问题
- 雷电3设备支持较不稳定。
- Airdrop 无效。


### Kexts

- [Lilu.kext 1.6.2](https://github.com/acidanthera/Lilu)
- [WhateverGreen.kext 1.6.1](https://github.com/acidanthera/WhateverGreen)
- [SMCProcessor.kext 1.3.0](https://github.com/acidanthera/VirtualSMC)
- [SMCSuperIO.kext 1.3.0](https://github.com/acidanthera/VirtualSMC)
- [VirtualSMC.kext 1.3.0](https://github.com/acidanthera/VirtualSMC)
- [AppleALC.kext 1.7.5](https://github.com/acidanthera/AppleALC)
- [IntelMausi.kext 1.0.7](https://github.com/acidanthera/IntelMausi)
- [AirportItlwm.kext 2.1.0](https://github.com/OpenIntelWireless/itlwm)
- [BlueToolFixup.kext 2.6.3](https://github.com/acidanthera/BrcmPatchRAM)
- [IntelBTPatcher.kext 2.2.0](https://github.com/OpenIntelWireless/IntelBluetoothFirmware)
- [IntelBluetoothFirmware.kext 2.2.0](https://github.com/OpenIntelWireless/IntelBluetoothFirmware)
- [IntelBluetoothInjector.kext 2.2.0](https://github.com/OpenIntelWireless/IntelBluetoothFirmware)
- [FakePCIID.kext 1.3.16](https://github.com/daliansky/OS-X-Fake-PCI-ID)
- [FakePCIID_Intel_HDMI_Audio.kext 1.3.16](https://github.com/daliansky/OS-X-Fake-PCI-ID)
- [IOElectrify.kext 1.0.0](https://github.com/the-darkvoid/macOS-IOElectrify)

### 工具

- [Hackintool](https://github.com/headkaze/Hackintool) 
- [OpenCore Configurator](https://mackie100projects.altervista.org/opencore-configurator/) 即 `OCC`。
- [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) 三码生成工具。
- [MountEFI](https://github.com/corpnewt/MountEFI) EFI 分区挂载工具。
- [EFI Agent](https://github.com/headkaze/EFI-Agent) 更方便的EFI分区挂载工具。
- [gibMacOS](https://github.com/corpnewt/gibMacOS) macOS 官方镜像下载工具。
- [ProperTree](https://github.com/corpnewt/ProperTree) Plist 编辑器。


### 技术交流

QQ群: 591528332


### Credits

Thanks to [HawkysCC](https://github.com/HawkysCC) and his [EFI](https://github.com/HawkysCC/Hackintosh-NUC10i7)
