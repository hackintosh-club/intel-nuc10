
## Intel NUC10 Hackintosh OpenCore EFI

### [简体中文](README.zh_CN.md)

### OpenCore

[OpenCore 0.9.2](https://github.com/acidanthera/OpenCorePkg)


### Adapted

- NUC10i7FNH/FNK
- NUC10i5FNH/FNK
- NUC10i3FNH/FNK


### OS Version Tested

- macOS Ventura 13.x (Default `config.plist`)
- macOS Monterey 12.x (Replace `config.plist` with `config.Monterey.plist`)


### BIOS config

**The latest version (after 0055) will make CFGLock.efi unable to work!!!**

**How to update BIOS to the latest version `0059` ?** 
1. Unlock CFG with `CFGLock` tool under BIOS `0055`, make sure the value of `CFG Lock` is `0` 
2. Update BIOS to the latest verion `0059` 
3. Enter `CFGLock`, Check whether the `CFG Lock` value is `0`, if it is, then you made it. 


BIOS version **FNCML357.0059(CFG Unlocked under 0055)**

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

keep other settings default.


### CFG Unlock

If it's the first time your nuc10 install with macOS, you must unlock CFG before install macOS.

1. Find a USB flash drive, formatted as `FAT32` partition.
2. Copy `EFI` files to the root of your USB drive, path will be `/EFI`.
3. Reboot your nuc10, press `F10`, boot with the drive above. 
4. Choose `CFGLock Shell.efi` unlock CFG. 

**When in the OC's booting interface, press the `space bar` to show more options**


### Known issue

- Thunderbolt 3 Support very buggy
- Continuity features not work(EXCEPT HandOff and Universal Clipboard).


### Kexts

- [Lilu.kext 1.6.5](https://github.com/acidanthera/Lilu)
- [SMCProcessor.kext 1.3.1](https://github.com/acidanthera/VirtualSMC)
- [SMCSuperIO.kext 1.3.1](https://github.com/acidanthera/VirtualSMC)
- [VirtualSMC.kext 1.3.1](https://github.com/acidanthera/VirtualSMC)
- [WhateverGreen.kext 1.6.4](https://github.com/acidanthera/WhateverGreen)
- [AppleALC.kext 1.8.2](https://github.com/acidanthera/AppleALC)
- [IntelMausi.kext 1.0.7](https://github.com/acidanthera/IntelMausi)
- [NVMeFix.kext 1.1.0](https://github.com/acidanthera/NVMeFix)
- [AirportItlwm.kext 2.2.0-alpha](https://github.com/OpenIntelWireless/itlwm)
- [BlueToolFixup.kext 2.6.6](https://github.com/acidanthera/BrcmPatchRAM)
- [IntelBTPatcher.kext 2.2.0](https://github.com/OpenIntelWireless/IntelBluetoothFirmware)
- [IntelBluetoothFirmware.kext 2.2.0](https://github.com/OpenIntelWireless/IntelBluetoothFirmware)
- [IntelBluetoothInjector.kext 2.2.0](https://github.com/OpenIntelWireless/IntelBluetoothFirmware)


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

- [HDMI Firmware Update Tool](https://www.intel.com/content/www/us/en/download/19639/intel-hdmi-firmware-update-tool-for-intel-nuc10i3fn-nuc10i5fn-nuc10i7fn-products.html)
- [Thunderbolt™ 3 Firmware Update Tool](https://www.intel.com/content/www/us/en/download/19794/thunderbolt-3-firmware-update-tool-for-nuc10ixfn.html)


### Discuss

QQ Group: 591528332


### Credits

Thanks to [HawkysCC](https://github.com/HawkysCC) and his [EFI](https://github.com/HawkysCC/Hackintosh-NUC10i7)
