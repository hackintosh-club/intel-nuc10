
## Intel NUC10 黑苹果 OpenCore EFI

### OpenCore

[OpenCore 0.6.5](https://github.com/acidanthera/OpenCorePkg)


### 适配机型

- NUC10i7FNH/FNK
- NUC10i5FNH/FNK
- NUC10i3FNH/FNK


### 可安装系统

- macOS Big Sur 11.1
- macOS Catalina 10.15.7 (需替换wifi驱动 `AirportItlwm.kext` 为 Catalina 版本)


### BIOS 设置

- Advanced -> Storage -> SATA Mode Selection -> AHCI
- Advanced -> Video -> IGD Minimum Memory -> 64MB
- Advanced -> Video -> IGD Aperture Size -> 256MB
- Advanced -> Video -> IGD Primary Video Port -> Auto
- Boot -> Secure Boot -> Secure Boot -> Disabled
- Boot -> Boot Priority -> UEFI Boot -> Checked
- Boot -> Boot Priority -> Legacy Boot -> Unchecked
- Boot -> Boot Priority -> Fast Boot -> Unchecked

其它默认设置即可。


### CFG Unlock

新机器或之前未安装过 macOS 的机器，需要解锁CFGLock，具体步骤如下：

1. 找一个U盘，格式化为 `FAT32` 分区。
2. 下载 `EFI` 文件，解压放到U盘根目录。（注意：目录结构应为`/EFI`）。
3. 将U盘插入NUC，重启，按`F10`，选择从刚才放入 `EFI` 文件的那个U盘启动。 
4. 选择 `CFGLock Shell.efi` 选择回车，进行解锁。

注意：若在OC引导界面看不到 `CFGLock Shell.efi` ，按`空格键`即可显示。


### config.plist

1. `/EFI/OC/config.plist` 默认文本启动模式，声卡驱动为 `AppleALC.kext`，有些情况下 HDMI 音频不能正常工作。
2. `/EFI/OC/config.VoodooHDA.plist` 默认文本启动模式，万能声卡驱动 `VoodooHDA.kext`(HDMI音频可以正常工作，内置麦克风也可以正常工作)。
3. `/EFI/OC/config.UI.plist` 图形界面启动模式，声卡驱动为 `AppleALC.kext`。
4. `/EFI/OC/config.UI.VoodooHDA.plist` 图形界面启动模式，万能声卡驱动 `VoodooHDA.kext`。

选择你自己喜欢的启动方式，替换掉 `config.plist` 即可。   
**在 OC 引导界面，按 `空格键` 可显示辅助功能**


### 已知问题

- 默认 `AppleALC.kext` 驱动下，部分设备HDMI音频无效（可使用万能声卡驱动 `VoodooHDA.kext` 解决)。
- Airdrop 无效。
- SD卡插槽无效。


### HDMI 音频

- 默认音频驱动为 `AppleALC.kext` 在 `/EFI/OC/config.plist` 中开启。 
- 如需使用万能声卡驱动 `VoodooHDA.kext`, 选择相应 plist 文件替换到 `/EFI/OC/config.plist` 即可。（别忘记替换三码）


### Kexts

- [AirportItlwm.kext v1.2.0](https://github.com/OpenIntelWireless/itlwm)
- [AppleALC.kext 1.5.6](https://github.com/acidanthera/AppleALC)
- [IntelBluetoothFirmware.kext 1.1.2](https://github.com/OpenIntelWireless/IntelBluetoothFirmware)
- [IntelBluetoothInjector.kext 1.1.2](https://github.com/OpenIntelWireless/IntelBluetoothFirmware)
- [IntelMausi.kext 1.0.5](https://github.com/acidanthera/IntelMausi)
- [Lilu.kext 1.5.0](https://github.com/acidanthera/Lilu)
- [SMCProcessor.kext 1.1.9](https://github.com/acidanthera/VirtualSMC)
- [SMCSuperIO.kext 1.1.9](https://github.com/acidanthera/VirtualSMC)
- [VirtualSMC.kext 1.1.9](https://github.com/acidanthera/VirtualSMC)
- [WhateverGreen.kext 1.4.6](https://github.com/acidanthera/WhateverGreen)
- [VoodooHDA.kext 2.9.2](https://github.com/chris1111/VoodooHDA-OC) 


### 工具

- [Hackintool](https://github.com/headkaze/Hackintool) 
- [OpenCore Configurator](https://mackie100projects.altervista.org/opencore-configurator/) 即 `OCC`。
- [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) 三码生成工具。
- [MountEFI](https://github.com/corpnewt/MountEFI) EFI 分区挂载工具。
- [gibMacOS](https://github.com/corpnewt/gibMacOS) macOS 官方镜像下载工具。
- [ProperTree](https://github.com/corpnewt/ProperTree) Plist 编辑器。


### 技术交流

QQ群: 591528332


### Credits

Thanks to [HawkysCC](https://github.com/HawkysCC) and his [EFI](https://github.com/HawkysCC/Hackintosh-NUC10i7)


