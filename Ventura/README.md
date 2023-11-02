# macOS Ventura (13.x)

Unfortunately, with the announcement of macOS Ventura, Apple has officially dropped support up to Skylake, including IGPU support.

The solution is to modify the config.plist and spoof the GPU properties SKL as KBL.

There is a more detailed description in my blog post (Chinese): [Skylake 如何吃上最新黑苹果 macOS  Ventura](https://banmiya.com/skylake-hackintosh)


## Support Versions

| macOS Versions | Build    | Support Status |
|----------------|----------|:--------------:|
| 13.0 beta 4    | 22A5311f |       ✅        |

Support Status Explanation：
* ✅ Fully supported, including developer versions
* ⚠️ Partially supported, consumer version only
* 🚧 Exploration in progress, not supported

## Notes of New Boot Args 

| Boot Args           | Notes                                                                      |
|---------------------|----------------------------------------------------------------------------|
| lilucpu=9           | Spoofs CPU Generation as KBL.                                              |
| -igfxsklaskbl	      | Spoofs GPU Generation as KBL.                                              |
| -disablegfxfirmware | To avoid firmware load endless loop                                        |
| -wegnoegpu          | To disable all external GPUs (NVIDIA and AMD). Mainly required on Laptops. |

## Images

![info](https://raw.githubusercontent.com/zmlu/Hackintosh-OC-Colorful-C.B150M-i5-6500-Skylake-HD530/main/Ventura/images/ventura_info.png "info")

![Stage Manager](https://raw.githubusercontent.com/zmlu/Hackintosh-OC-Colorful-C.B150M-i5-6500-Skylake-HD530/main/Ventura/images/ventura_stage_manager.png "Stage Manager")

## SMBIOS

iMac 18,1

## OpenCore Version

| Kext                       | Version              |
|----------------------------|----------------------|
| OpenCore                   | 0.9.1-852016c        |
| AppleALC.kext              | 1.8.1-274381c        |
| Lilu.kext                  | 1.6.5-3f61754        |
| VirtualSMC.kext            | 1.3.2-87e726c        |
| WhateverGreen.kext         | 1.6.5-6aaea33        |
| CPUFriend.kext             | 1.2.6                |
| CPUFriendDataProvider.kext | Mac-4B682C642B45593E |
| FeatureUnlock.kext         | 1.1.4-ec664b2        |

## Update Log

* 2023.03.29
  * Update OpenCore and Kexts versions.

* 2022.06.20
  * Fix bug: installation failed via OTA.
  * Update OC: support `AvoidRuntimeDefrag` on Ventura.
  * WhateverGreen support `-igfxsklaskbl` boot args, so drop `SKLAsKBLGraphicsInfo.kext`.

* 2022.06.16
    * New Config Support macOS 13 (Ventura) 🎉
