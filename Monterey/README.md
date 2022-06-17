# macOS Monterey (12.x)

## Support Versions

| macOS Versions | Build    | Support Status |
|----------------|----------|:--------------:|
| 12.0           | 21A344   |       ✅        |
| 12.0.1         | 21A559   |       ✅        |
| 12.1           | 21C52    |       ✅        |
| 12.2           | 21D49    |       ✅        |
| 12.2.1         | 21D62    |       ✅        |
| 12.3           | 21E230   |       ✅        |
| 12.3.1         | 21E258   |       ✅        |
| 12.4           | 21F79    |       ✅        |
| 12.5 beta 2	   | 21G5037d |       ✅        |
| 12.5 beta 3	   | 21G5046c |       ✅        |

Support Status Explanation：
* ✅ Fully supported, including developer versions
* ⚠️ Partially supported, consumer version only
* 🚧 Exploration in progress, not supported

## SMBIOS

iMac 17,1

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

## What does NOT work ⚠️

* Sleep - Sleeps but won't wake

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