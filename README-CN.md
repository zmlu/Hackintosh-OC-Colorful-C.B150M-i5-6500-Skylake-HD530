# Hackintosh-OC-Colorful-C.B150M-i5-6500-Skylake-HD530

公司电脑黑苹果OpenCore配置

*其他语言版本: [English](README.md), [简体中文](README-CN.md).*

## 支持系统

* macOS Monterey 12.3 (21E230)

## 公司电脑配置

* 主板厂商：Colorful Technology And Development Co.,LTD
* 主板型号：Battle Axe C.B150M-HD
* 主板系统版本：V20
* 主板芯片组：Intel Sunrise Point B150, Intel Skylake-S

* CPU：Intel(R) Core(TM) i5-6500 CPU @ 3.20GHz
* 显卡：Intel HD Graphics 530
* 独显：无
* 声卡：Realtek ALC662

* 内存1：Tigo-2133Mhz-8G-DDR4
* 内存2：Tigo-2133Mhz-8G-DDR4

* 硬盘1：HDD：KINGSTON SA400S37240G  (240 GB, SATA-III)
* 硬盘2：SSD：WDC WD10EZEX-75WN4A0  (1 TB, 7200 RPM, SATA-III)

详细配置见Report.txt

## 主板配置

如果你跟我的主板型号和系统版本一样可以参考括号中的位置，使用shell修改

### 禁用

* CFG lock (0x11F 设为 0x0)
* VT-d (0x496 设为 0x0)
* SGX (0x1CA 设为 0x0)
* CSM (0xE17 设为 0x0)
* RTC Lock (0x5A5 设为 0x0)

### 启用

* Above 4G Decoding (0xDEC 设为 0x1)
* Hyper-threading (0xE9 设为 0x1)
* Execute Disable Bit (0x272 设为 0x1)
* EHCI Hand-off (0x2 设为 0x1)

## OpenCore及相关驱动软件版本

* OpenCore 0.7.9-c91eebf
* AppleALC.kext 1.7.0
* Lilu.kext 1.5.9-bd48fa7
* VirtualSMC.kext 1.2.9
* WhateverGreen.kext 1.5.8
* RealtekRTL8111.kext V2.4.2
* AppleMCEReporterDisabler.kext
* CPUFriend.kext 1.2.5
* CPUFriendDataProvider.kext (Mac-7BA5B2D9E42DDD94)
* FeatureUnlock.kext 1.0.7

## 更新日志

* 2022.03.08
  * 更新 OpenCore 为 0.7.9-c91eebf 开发版
  * 更新 AppleALC.kext、Lilu.kext、VirtualSMC.kext、WhateverGreen.kext、CPUFriend.kext
  
* 2022.01.05
  * 更新 OpenCore 为 0.7.7-027a2ef 开发版
  * 更新 AppleALC.kext、Lilu.kext、VirtualSMC.kext、WhateverGreen.kext

* 2021.11.15
  * 更新 OpenCore 为 0.7.6-f2bc242 开发版
  * 修改 SMBIOS 为 iMacPro1,1 来解锁 Apple Music Lossless 格式播放
  * 因为更新了SMBIOS 删除 USBPorts.kext 新增 USBInjectAll.kext
  * 因为更新 SMBIOS 新增 AppleMCEReporterDisabler.kext，防止内核崩溃
  * 新增 CPUFriend.kext、CPUFriendDataProvider.kext 来实现睿频

* 2021.11.05
  * 更新 OpenCore 为 0.7.5 和 Kext 驱动

* 2021.08.06
  * 新增配置
