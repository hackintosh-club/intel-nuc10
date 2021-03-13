
## Intel NUC10 Hackintosh OpenCore EFI

[![Gitter](https://badges.gitter.im/hackintosh-efi/intel-nuc10.svg)](https://gitter.im/hackintosh-efi/intel-nuc10?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)

### [简体中文](README.zh_CN.md)

### OpenCore

[OpenCore 0.6.7](https://github.com/acidanthera/OpenCorePkg)


### Adapted

- NUC10i7FNH/FNK
- NUC10i5FNH/FNK
- NUC10i3FNH/FNK


### OS Version Tested

- macOS Big Sur 11.1
- macOS Catalina 10.15.7 (Need to replace `AirportItlwm.kext` to Catalina version)


### BIOS config

BIOS version **FNCML357.0050 (latest)**

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
    * Deep S4/S5 -> Off
    * Wake on Lan from S4/S5 -> Stay Off
    * Wake System from S5 -> Off
    * Wake From Thunderbolt Device -> Off

keep other settings default.


### CFG Unlock

If it's the first time your nuc10 install with macOS, you must unlock CFG before install macOS.

1. Find a USB flash drive, formatted as `FAT32` partition.
2. Copy `EFI` files to the root of your USB drive, path will be `/EFI`.
3. Reboot your nuc10, press `F10`, boot with the drive above. 
4. Choose `CFGLock Shell.efi` unlock CFG. 


### config.plist

1. `/EFI/OC/config.plist` Default boot with `AppleALC.kext`.
2. `/EFI/OC/config.AppleALC.plist` same as `/EFI/OC/config.plist`.
3. `/EFI/OC/config.VoodooHDA.plist` Default boot with `VoodooHDA.kext`(HDMI Audio works).
4. `/EFI/OC/config.GUI.AppleALC.plist` GUI boot with `AppleALC.kext`.
5. `/EFI/OC/config.GUI.VoodooHDA.plist` GUI boot with `VoodooHDA.kext`(HDMI Audio works).

Choose one you prefer to :)   

**When in the OC's booting interface, press the `space bar` to show more options**


### Known issue

- HDMI Audio not work(you can use VoodooHDA.kext as alternative).
- Airdrop not work.
- SD Card not work.


### HDMI Audio

- The default Audio drive is `AppleALC.kext` loaded by the file `/EFI/OC/config.plist`.
- If you want to use `VoodooHDA.kext`, just rename the file `/EFI/OC/config.VoodooHDA.plist` to `/EFI/OC/config.plist`. (Do not forget to replace the GMBIOS with your own.)


### Kexts

- [AirportItlwm.kext v1.2.0](https://github.com/OpenIntelWireless/itlwm)
- [AppleALC.kext 1.5.8](https://github.com/acidanthera/AppleALC)
- [IntelBluetoothFirmware.kext 1.1.2](https://github.com/OpenIntelWireless/IntelBluetoothFirmware)
- [IntelBluetoothInjector.kext 1.1.2](https://github.com/OpenIntelWireless/IntelBluetoothFirmware)
- [IntelMausi.kext 1.0.5](https://github.com/acidanthera/IntelMausi)
- [Lilu.kext 1.5.1](https://github.com/acidanthera/Lilu)
- [SMCProcessor.kext 1.2.1](https://github.com/acidanthera/VirtualSMC)
- [SMCSuperIO.kext 1.2.1](https://github.com/acidanthera/VirtualSMC)
- [VirtualSMC.kext 1.2.1](https://github.com/acidanthera/VirtualSMC)
- [WhateverGreen.kext 1.4.8](https://github.com/acidanthera/WhateverGreen)
- [VoodooHDA.kext 2.9.2](https://github.com/chris1111/VoodooHDA-OC) 


### Tools

- [Hackintool](https://github.com/headkaze/Hackintool) 
- [OpenCore Configurator](https://mackie100projects.altervista.org/opencore-configurator/) AKA OCC.
- [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) Generate SMBIOS.
- [MountEFI](https://github.com/corpnewt/MountEFI) Mount EFI partation.
- [gibMacOS](https://github.com/corpnewt/gibMacOS) Build your own MacOS image.
- [ProperTree](https://github.com/corpnewt/ProperTree) Plist editor.


### Discuss

QQ Group: 591528332


### Credits

Thanks to [HawkysCC](https://github.com/HawkysCC) and his [EFI](https://github.com/HawkysCC/Hackintosh-NUC10i7)


### By me a beer

![alipay](https://sn3301files.storage.live.com/y4motdhk_seImaIqjpenUPgmDei226yPQ5oylU0MjSq0izM6oM4IOIfUhfos1JRhtDsf3UmRcqNuJCGGV30byvRD19hW3hHkPRNs38D0XTnN0EriFrmKWjjPzj-gCJ-oSZ-9eY-0yIaFHyb2RzAzhza-lV2bfbr9WN-nbOId_FCLijghCsFpshvmq18PyJf7xWj?width=128&height=128&cropmode=none) 
Alipay

![wepay](https://sn3301files.storage.live.com/y4mfSVsBSWF0tZ_ieHI-ISXnGu5YYUC7AhfEpqF6TFDkkOamY3nLjdrYGQZ_ypY2UnHJ_PbbBmiJOLaQzX2mdlEYTrs8fublvjpM2uXiHmu0f0_DSjxcQS5pLNfHN6e6uvZEd_s5qgE0Et953Da767VI5HhlnvUlbyEq3f_DNd8gFNgDkDQDLIzZDmctsVB1DVo?width=128&height=128&cropmode=none) 
Wechat Pay

[Paypal](https://www.paypal.me/mrasong) 

