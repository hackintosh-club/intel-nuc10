
## Intel NUC10 Hackintosh OpenCore EFI

[![Gitter](https://badges.gitter.im/hackintosh-efi/intel-nuc10.svg)](https://gitter.im/hackintosh-efi/intel-nuc10?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)

### [简体中文](README.zh_CN.md)

### OpenCore

[OpenCore 0.7.1](https://github.com/acidanthera/OpenCorePkg)


### Adapted

- NUC10i7FNH/FNK
- NUC10i5FNH/FNK
- NUC10i3FNH/FNK


### OS Version Tested

- macOS Big Sur
  * 11.4
  * 11.5
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

- [AirportItlwm.kext 1.3.0](https://github.com/OpenIntelWireless/itlwm)
- [AppleALC.kext 1.6.2](https://github.com/acidanthera/AppleALC)
- [IntelBluetoothFirmware.kext 1.1.3](https://github.com/OpenIntelWireless/IntelBluetoothFirmware)
- [IntelBluetoothInjector.kext 1.1.3](https://github.com/OpenIntelWireless/IntelBluetoothFirmware)
- [IntelMausi.kext 1.0.7](https://github.com/acidanthera/IntelMausi)
- [Lilu.kext 1.5.3](https://github.com/acidanthera/Lilu)
- [SMCProcessor.kext 1.2.5](https://github.com/acidanthera/VirtualSMC)
- [SMCSuperIO.kext 1.2.5](https://github.com/acidanthera/VirtualSMC)
- [VirtualSMC.kext 1.2.5](https://github.com/acidanthera/VirtualSMC)
- [WhateverGreen.kext 1.5.1](https://github.com/acidanthera/WhateverGreen)
- [VoodooHDA.kext 2.9.2](https://github.com/chris1111/VoodooHDA-OC) 
- [FakePCIID.kext 1.3.15](https://bitbucket.org/RehabMan/os-x-fake-pci-id)
- [FakePCIID_Intel_HDMI_Audio.kext 1.3.15](https://bitbucket.org/RehabMan/os-x-fake-pci-id)
- [IOElectrify.kext 1.0.0](https://github.com/the-darkvoid/macOS-IOElectrify)

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
