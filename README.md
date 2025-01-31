
## Intel NUC10 Hackintosh OpenCore EFI

### [简体中文](README.zh_CN.md)

### OpenCore

[OpenCore 1.0.3](https://github.com/acidanthera/OpenCorePkg)


### Adapted

- NUC10i7FNH/FNK
- NUC10i5FNH/FNK
- NUC10i3FNH/FNK


### OS Version Tested

- macOS Sequoia 15.x **(WiFi Need [OCLP-Mod by laobamac](https://github.com/hackintosh-club/intel-nuc10/releases/tag/oclp) Patch)**
- macOS Sonoma 14.x 
- macOS Ventura 13.x
- macOS Monterey 12.x
- macOS BigSur 11.x
- macOS Catalina 10.15.x


### BIOS config

**The latest version (after 0055) will make CFGLock.efi unable to work!!!**

**How to update BIOS to the latest version `0059` ?** 
1. Unlock CFG with `CFGLock` tool under BIOS `0055`, make sure the value of `CFG Lock` is `0` 
2. Update BIOS to the latest verion `0059` 
3. Enter `CFGLock`, Check whether the `CFG Lock` value is `0`, if it is, then you made it. 


BIOS version **FNCML357.0061(CFG Unlocked under 0055)**

+ Advanced
  - Storage
    * SATA Mode Selection -> AHCI
  - Video
    * IGD Minimum Memory -> 64MB
    * IGD Aperture Size -> 512MB
    * IGD Primary Video Port -> `Thunderbolt` or `HDMI` (Depends on your default monitor)
    * IGD Secondary Video Port -> None
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
    * Wake on Lan from S4/S5 -> Power On - Normal Boot
    * Wake System from S5 -> Off
    * Wake From Thunderbolt Device -> Off

keep other settings default.


### CFG Unlock

If it's the first time your nuc10 install with macOS, you must unlock CFG before install macOS.

1. Find a USB flash drive, formatted as `FAT32` partition.
2. Copy `EFI` files to the root of your USB drive, path will be `/EFI`.
3. Reboot your nuc10, press `F10`, boot with the drive above. 
4. Choose `CFGLock Shell.efi` unlock CFG. 

**When in the OC's booting interface, press the `space bar` to show more options**


### Known issue

- Thunderbolt 3 device does not support hot swap.
- Continuity features not work(EXCEPT HandOff and Universal Clipboard).


### Screenshot

![macOS](Screenshot/about.jpg)

![Info](Screenshot/info.jpg)

![Thunderbolt3](Screenshot/thunderbolt3.jpg)

![Geekbench6](Screenshot/geekbench6.jpg)


### Kexts

- [Lilu.kext](https://github.com/acidanthera/Lilu)
- [SMCProcessor.kext](https://github.com/acidanthera/VirtualSMC)
- [SMCSuperIO.kext](https://github.com/acidanthera/VirtualSMC)
- [VirtualSMC.kext](https://github.com/acidanthera/VirtualSMC)
- [WhateverGreen.kext](https://github.com/acidanthera/WhateverGreen)
- [AppleALC.kext](https://github.com/acidanthera/AppleALC)
- [IntelMausi.kext](https://github.com/acidanthera/IntelMausi)
- [AirportItlwm.kext](https://github.com/OpenIntelWireless/itlwm)
- [BlueToolFixup.kext](https://github.com/acidanthera/BrcmPatchRAM)
- [IntelBTPatcher.kext](https://github.com/OpenIntelWireless/IntelBluetoothFirmware)
- [IntelBluetoothFirmware.kext](https://github.com/OpenIntelWireless/IntelBluetoothFirmware)
- [IntelBluetoothInjector.kext](https://github.com/OpenIntelWireless/IntelBluetoothFirmware)


### Tools

- [Hackintool](https://github.com/headkaze/Hackintool) 
- [OCAuxiliaryTools](https://github.com/ic005k/OCAuxiliaryTools) AKA `OCAT`.
- [OpenCore Configurator](https://mackie100projects.altervista.org/opencore-configurator/) AKA `OCC`.
- [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) Generate SMBIOS.
- [MountEFI](https://github.com/corpnewt/MountEFI) Mount EFI partition.
- [EFI Agent](https://github.com/headkaze/EFI-Agent) Better EFI partition mount App.
- [gibMacOS](https://github.com/corpnewt/gibMacOS) Build your own MacOS image.
- [ProperTree](https://github.com/corpnewt/ProperTree) Plist editor.


### Drive

- [BIOS & Firmware](https://www.asus.com.cn/supportonly/nuc10i7fnh/helpdesk_bios/) 


### OC Theme

[BsxM1](https://github.com/blackosx/BsxM1)


### Discuss

QQ Group: 591528332


### Credits

Thanks to [HawkysCC](https://github.com/HawkysCC) and his [EFI](https://github.com/HawkysCC/Hackintosh-NUC10i7)
