# Hackintosh-OC-Colorful-C.B150M-i5-6500-Skylake-HD530

公司电脑黑苹果OpenCore配置

## 支持系统

* macOS Monterey beta 12.0 (21A5294g)
* macOS Big Sur 11.5.1 (20G80)

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

* OpenCore 7.1

## 更新日志

* 2021.08.06 新增配置