
## Intel NUC10 Hackintosh OpenCore EFI

### OpenCore

[OpenCore 0.6.5](https://github.com/acidanthera/OpenCorePkg)


### Adapted

- NUC10i7FNH/FNK
- NUC10i5FNH/FNK
- NUC10i3FNH/FNK


### OS Version Tested

- macOS Big Sur 11.1
- macOS Catalina 10.15.7 (Need to replace `AirportItlwm.kext` to Catalina version)


### config.plist

- `/EFI/OC/config.plist` Default boot with `AppleALC.kext`.
- `/EFI/OC/config.VoodooHDA.plist` Default boot with `VoodooHDA.kext`(HDMI Audio works).
- `/EFI/OC/config.UI.plist` UI boot with `AppleALC.kext`.
- `/EFI/OC/config.UI.VoodooHDA.plist` UI boot with `VoodooHDA.kext`(HDMI Audio works).

Choose one you prefer :)   
**To display more boot items, print `Space` key.**


### Known issue

- HDMI Audio not work(you can use VoodooHDA.kext as alternative).
- Airdrop not work.
- SD Card not work.


### HDMI Audio

 - The default Audio drive is `AppleALC.kext` loaded by the file `/EFI/OC/config.plist`.
 - If you want to use `VoodooHDA.kext`, just rename the file `/EFI/OC/config.VoodooHDA.plist` to `/EFI/OC/config.plist`. (Do not forget to replace the GMBIOS with your own.)


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


### Tools

- [Hackintool](https://github.com/headkaze/Hackintool) 
- [OpenCore Configurator](https://mackie100projects.altervista.org/opencore-configurator/) AKA OCC.
- [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) Generate SMBIOS.
- [MountEFI](https://github.com/corpnewt/MountEFI) Mount EFI partation.
- [gibMacOS](https://github.com/corpnewt/gibMacOS) Build your own MacOS image.
- [ProperTree](https://github.com/corpnewt/ProperTree) Plist editor.


### Credits

Thanks to [HawkysCC](https://github.com/HawkysCC) and his [EFI](https://github.com/HawkysCC/Hackintosh-NUC10i7)
