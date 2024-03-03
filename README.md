# Pavilion 15t-cs0 Hackintosh

This OpenCore config works for HP Pavilion 15t-cs0

## Credits

* [OpenCore](https://github.com/acidanthera/OpenCorePkg) Boot
* [Lilu.kext](https://github.com/acidanthera/Lilu/releases/latest)
* [OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/config-laptop.plist/coffee-lake.html)
* [Writeup Template](https://github.com/dragonflylee/Yoga730-hackintosh)

## What is not working
NVIDIA GeForce MX150 - NVIDIA!
MacOS Sonoma - Kaby Lake 7th gen not supported!
## What is half working
ELAN Touchpad - Sometimes stops working and I need to put the computer into sleep mode and log in again.
Wake up from sleep - I have to click the trackpad or a button on the keyboard to wake the computer up, simply opening the lid does not wake it up.
## What is Working
* Intel Core i7-7500U with Intel HD Graphics 620: [WhateverGreen.kext](https://github.com/acidanthera/WhateverGreen/releases/latest)
* Realtek ALC295 inject Layout-id `13` [AppleALC.kext](https://github.com/acidanthera/AppleALC/releases/latest)
* PS2 Keyboard  [VoodooPS2Controller.kext](https://github.com/acidanthera/VoodooPS2/releases/latest)
* TouchPad and TouchScreen work, [VoodooI2C.kext](https://github.com/alexandred/VoodooI2C/releases/latest)
* Battery and cpu sensor, [VirtualSMC.kext](https://github.com/acidanthera/VirtualSMC/releases/latest).
* [BrightnessKeys.Kext](https://github.com/acidanthera/BrightnessKeys/releases/latest)
* [NVMeFix.kext](https://github.com/acidanthera/NVMeFix/releases/latest)
* [SystemProfilerMemoryFixup.kext](https://github.com/Goldfish64/SystemProfilerMemoryFixup)
* Intel Dual Band Wireless-AC 7265 (Wifi) [AirportItlwm.kext](https://github.com/OpenIntelWireless/itlwm/releases/latest)
* Intel Dual Band Wireless-AC 7265 (Bluetooth) [BlueToolFixUp.kext](https://github.com/acidanthera/BrcmPatchRAM/releases/latest), [IntelBluetoothFirmware](https://github.com/OpenIntelWireless/IntelBluetoothFirmware/releases/latest)
## [Pre-built SSDTs](https://dortania.github.io/Getting-Started-With-ACPI/ssdt-methods/ssdt-prebuilt.html#laptop-skylake-and-kaby-lake)
* [SSDT-PLUG-DRTNIA](https://github.com/dortania/Getting-Started-With-ACPI/blob/master/extra-files/compiled/SSDT-PLUG-DRTNIA.aml)
* [SSDT-EC-USBX-LAPTOP](https://github.com/dortania/Getting-Started-With-ACPI/blob/master/extra-files/compiled/SSDT-EC-USBX-LAPTOP.aml)
* [SSDT-PNLF](https://github.com/dortania/Getting-Started-With-ACPI/blob/master/extra-files/compiled/SSDT-PNLF.aml)
* [SSDT-XOSI](https://github.com/dortania/Getting-Started-With-ACPI/blob/master/extra-files/compiled/SSDT-XOSI.aml)
## BIOS setting before install
* Disable Security -> Secure Boot
* Switch RAID to AHCI in Configuration -> SATA Controller Mode (Preset)
## To fix internal hard drive not being detected during install
* [CtlnaAHCIPort.kext](https://github.com/dortania/OpenCore-Install-Guide/blob/master/extra-files/CtlnaAHCIPort.kext.zip)


## FAQ

- Q: Why am I getting a prohibited logo when trying to install MacOS Sonoma?
  A: MacOS Sonoma is not supported for this processor.
