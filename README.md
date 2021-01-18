
## Intel NUC10 Hackintosh OpenCore

Intel NUC10 OpenCore EFI

[OpenCore 0.6.5](https://github.com/acidanthera/OpenCorePkg)


#### Adapted

 - NUC10i5FNH
 - NUC10i5FNK
 - NUC10i7FNH
 - NUC10i7FNK


### Known issue

- HDMI Audio not work(you can use VoodooHDA.kext as alternative).
- Airdrop not work.
- SD Card not work.

#### HDMI Audio

 - The default Audio drive use `AppleALC.kext` loaded by the file `/EFI/OC/config.plist`.
 - If you want to use `VoodooHDA.kext`, just rename the file `/EFI/OC/config.VoodooHDA.plist` to `/EFI/OC/config.plist`.


### kexts update

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

