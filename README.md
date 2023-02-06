## 配置信息

理论上幽灵峡谷其他型号都可以正常使用，使用前请修改三码（非i7版本还需CPU型号）

- **无线网卡：** BCM943602CS三天线版（免驱）
- **内存：** 金百达 DDR4 3200MHz 16GB x2
- **显卡：** 撼迅 6600XT 竞技（免驱）
- **硬盘：** 金百达 KP260 1T SSD（TRIM正常）

机型选择为 Mac mini 2018，因为NUC本身就更像Mac mini，并且在系统设置里面，也会显示为Mac mini对应的图标。

![image-20230201150208516](https://s2.loli.net/2023/02/01/rNBWVTsvJy9zLMt.png)

***

## 完善情况

* [x] 无线网卡为白果卡，使用M.2转接卡安装，蓝牙和WiFi正常驱动，支持隔空投送、通用控制、连续互通等。
* [x] 核显正常驱动，可以使用算力板的HDMI口输出，频率正常，硬件解码正常，Final Cut Pro导出H.264格式核显能够满载，随航功能正常。
* [x] 独显正常驱动，所有输出接口（3xDP，1xHDMI）均可使用，启动时第二阶段会正常读条进系统，不会黑屏。
* [x] USB接口已经定制，包括白苹果网卡的蓝牙数据线需要使用的算力板内部迷你4pin接口，两个雷电接口正常使用（Titan Ridge目前无法直接在系统信息中显示雷雳树，需要刷固件，这会导致Windows下无法使用，故没有折腾）
* [x] 声卡使用id为68，正常使用，包括光纤口和普通音频口。
* [x] 休眠唤醒正常（建议系统设置中关闭电源小憩，否则会时不时自动唤醒又休眠）
* [x] 板载有线网口正常，其中一个是千兆接口，还有一个是2.5G接口。
* [x] 读卡器正常，系统信息中会显示读卡器信息。
* [x] 支持白苹果开机音频、OC图形界面与白苹果一致，默认跳过选择界面（启动时按住ALT键进入选择界面）

⚠️ **特别注意：**

* NUC9存在高清启动问题，对显卡和显示器非常挑剔，两者只要有一个有问题，就会导致无法高清启动，即使你是4K显示器，开机会显示巨大骷髅头，分辨率被强制锁定在1024x768，只有进入系统加载完显卡驱动之后才会正常显示（只用核显就没有这个问题）此问题跟系统无关，是属于这个机器本身的问题，除了更换显卡或显示器之外无解，但愿各位不要出现，当然这个不影响正常使用，但是会影响强迫症患者。
  * 目前已经测试出现问题的独显型号：RX5500XT公版（所有接口无法高清启动）、华擎6600/6600XT CLI（所有接口无法高清启动）
  * 目前已经测试可以正常使用的独显型号：撼迅6600/6600XT（DP口可以正常高清启动，HDMI无法高清启动）
* 使用M.2转接的白苹果网卡，部分转接板会出现休眠之后断电的情况，这样就会导致无法蓝牙设备唤醒，只能使用有线设备连接USB口唤醒或是按一下机箱电源键唤醒。

***

## BIOS设置

目前的BIOS版本：0071

* Advance
  * Onboard Devices
    * WLAN：取消勾选（已安装白果卡）
    * Bluetooth：取消勾选（已安装白果卡）
  * Vedio
    * Primary Display：IGFX
    * Internal Graphics：Enabled
  * PCIE Bifurcation Configuration：Force x16（用不到那么多PCIE插槽，我把x16全给显卡了，自己看情况决定吧）
* Security
  * Intel Software Guard Extensions（SGX）：Disabled
* Boot
  * Secure Boot：Disabled

***

## 系统信息界面

![image-20230201152835634](https://s2.loli.net/2023/02/01/oZbGOkHmAY6erBV.png)

![image-20230201152502351](https://s2.loli.net/2023/02/01/ioqPxuVwMI87mZ5.png)

![image-20230201152513557](https://s2.loli.net/2023/02/01/hrRbaASQ8l5ciXJ.png)

![image-20230201152533023](https://s2.loli.net/2023/02/01/aHNYSg8fcTsjGe6.png)

![image-20230201152546094](https://s2.loli.net/2023/02/01/1fxKHp9EFPcDgs3.png)

![image-20230201152604391](https://s2.loli.net/2023/02/01/s7vToZI5rGnJz3P.png)

![image-20230201152614162](https://s2.loli.net/2023/02/01/jP6uMC5pXtey9Or.png)

![image-20230201152623641](https://s2.loli.net/2023/02/01/RcHeGEx8ZVL3iOI.png)

![image-20230201152645256](https://s2.loli.net/2023/02/01/T8zIsp4d3JLuAQe.png)

![image-20230201152655351](https://s2.loli.net/2023/02/01/r6jgJQwVSDMBq8N.png)

![image-20230201152932779](https://s2.loli.net/2023/02/01/sKPjl8xzHRkGwaf.png)
