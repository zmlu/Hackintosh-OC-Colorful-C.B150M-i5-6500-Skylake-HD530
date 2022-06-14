# Hackintosh-OC-Colorful-C.B150M-i5-6500-Skylake-HD530

Company computer's Hackintosh OpenCore configuration

*Read this in other languages: [English](README.md), [简体中文](README-CN.md).*

## Support macOS Versions

* macOS Monterey 12.5 Beta (21G5037d)

## Company Computer Hardware

* Motherboard Brand: Colorful Technology And Development Co.,LTD
* Motherboard Model: Battle Axe C.B150M-HD
* Motherboard Version: V20
* Motherboard Chipset: Intel Sunrise Point B150, Intel Skylake-S

* CPU: Intel(R) Core(TM) i5-6500 CPU @ 3.20GHz
* Graphics Card: Intel HD Graphics 530
* Nvidia/AMD Graphics Card: None
* Audio Card：Realtek ALC662

* Memory Slot 1: Tigo-2133Mhz-8G-DDR4
* Memory Slot 2: Tigo-2133Mhz-8G-DDR4

* Hard Disk 1: HDD：KINGSTON SA400S37240G  (240 GB, SATA-III)
* Hard Disk 2: SSD：WDC WD10EZEX-75WN4A0  (1 TB, 7200 RPM, SATA-III)

See detailed configuration at Report.txt(CN)

## BIOS Configuration

If you have the same as my motherboard model and system version, you can refer to the position in the brackets and use the BIOS shell to modify.

### Disabled

* CFG lock (0x11F Set to 0x0)
* VT-d (0x496 Set to 0x0)
* SGX (0x1CA Set to 0x0)
* CSM (0xE17 Set to 0x0)
* RTC Lock (0x5A5 Set to 0x0)

### Enabled

* Above 4G Decoding (0xDEC Set to 0x1)
* Hyper-threading (0xE9 Set to 0x1)
* Execute Disable Bit (0x272 Set to 0x1)
* EHCI Hand-off (0x2 Set to 0x1)

## OpenCore Version

| Kext                       | Version              |
|----------------------------|----------------------|
| OpenCore                   | 0.8.2                |
| AppleALC.kext              | 1.7.3                |
| Lilu.kext                  | 1.6.1                |
| VirtualSMC.kext            | 1.3.0                |
| WhateverGreen.kext         | 1.6.0                |
| CPUFriend.kext             | 1.2.6                |
| CPUFriendDataProvider.kext | Mac-DB15BD556843C820 |
| FeatureUnlock.kext         | 1.0.9                |

## CPUFriendDataProvider.kext Shell

```shell
./ResourceConverter.sh --kext /System/Library/Extensions/IOPlatformPluginFamily.kext/Contents/PlugIns/X86PlatformPlugin.kext/Contents/Resources/Mac-DB15BD556843C820.plist
```

## Update Log

* 2022.06.14
  * Update OpenCore 为 0.8.2 development version
  * Update Kext

* 2022.05.13
  * Update OpenCore 为 0.8.1-59fd524 development version
  * Update AppleALC.kext、Lilu.kext、VirtualSMC.kext、WhateverGreen.kext、CPUFriend.kext、FeatureUnlock.kext

* 2022.03.08
  * Update OpenCore to 0.7.9-c91eebf development version
  * Update AppleALC.kext、Lilu.kext、VirtualSMC.kext、WhateverGreen.kext、CPUFriend.kext

* 2022.01.05
  * Update OpenCore to 0.7.7-027a2ef development version
  * Update AppleALC.kext, Lilu.kext, VirtualSMC.kext, WhateverGreen.kext

* 2021.11.15
  * Update OpenCore to 0.7.6-f2bc242 development version
  * Modified SMBIOS to iMacPro1,1 to unlock Apple Music Lossless format playback
  * Removed USBPorts.kext because of updated SMBIOS and added USBInjectAll.kext
  * Because of updated SMBIOS Added AppleMCEReporterDisabler.kext to prevent kernel crash
  * Added CPUFriend.kext, CPUFriendDataProvider.kext to enable RWD

* 2021.11.05
  * Update OpenCore to 0.7.5 and Kext driver

* 2021.08.06
  * New configuration
