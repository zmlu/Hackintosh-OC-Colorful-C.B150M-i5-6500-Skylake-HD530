# macOS Ventura (13.x)

Unfortunately, with the announcement of macOS Ventura, Apple has officially dropped support up to Skylake, including IGPU support.

The solution is to modify the config.plist and spoof the GPU properties SKL as KBL.

## Support Versions

| macOS Versions | Build    | Support Status |
|----------------|----------|:--------------:|
| 13.0 beta 1    | 22A5266r |       ✅        |

Support Status Explanation：
* ✅ Fully supported, including developer versions
* ⚠️ Partially supported, consumer version only
* 🚧 Exploration in progress, not supported

## Notes of New Boot Args 

| Boot Args           | Notes                                                                      |
|---------------------|----------------------------------------------------------------------------|
| lilucpu=9           | Spoofs CPU Generation as KBL.                                              |
| -disablegfxfirmware | To avoid firmware load endless loop                                        |
| -wegnoegpu          | To disable all external GPUs (NVIDIA and AMD). Mainly required on Laptops. |

## SMBIOS

iMac 18,1

## OpenCore Version

| Kext                       | Version              |
|----------------------------|----------------------|
| OpenCore                   | 0.8.2-714fc69        |
| AppleALC.kext              | 1.7.3                |
| Lilu.kext                  | 1.6.1-9775e8b        |
| VirtualSMC.kext            | 1.3.0                |
| WhateverGreen.kext         | 1.6.0                |
| CPUFriend.kext             | 1.2.6                |
| CPUFriendDataProvider.kext | Mac-4B682C642B45593E |
| FeatureUnlock.kext         | 1.0.9                |

## Update Log

* 2022.06.20
  * Fix bug: installation failed via OTA.
  * Update OC: support `AvoidRuntimeDefrag` on Ventura.

* 2022.06.16
    * New Config Support macOS 13 (Ventura) 🎉
