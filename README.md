# Lenovo-Xiaoxin-Air14-IKBR-Opencore
-----------------------------------------------------------------------------------------------------
配置

[CPU] Intel i7-8550U  
[GPU] UHD620+Nvidia mx150（已屏蔽）  
[无线网卡] AC3165

-----------------------------------------------------------------------------------------------------
Opencore说明

1. 支持macOS 11.0 Big Sur

2. 触摸板正常

3. 睡眠正常

4. AC3165蓝牙+Wi-Fi基本正常，但是无法连接某些特殊热点，具体情况搞不明白

5. Opencore版本：0.7.3

-----------------------------------------------------------------------------------------------------
注意事项

1. 请自行解锁CFG Lock，设置DVMT 64M（重要），教程链接附在后面

**若未解锁CFG Lock，请勾选Kernel/Quirks/AppleCpuPmCfgLock及AppleXcpmCfgLock**

2. USB已定制(在此感谢hojiang23)，但最好请自行定制

3. 机型设置为Macbook Pro 15.2，请自行添加smbios信息

4. 最好不要用opencore引导其它系统，因为ACPI中的信息都会传递给操作系统

5. setup_var无法修改本机的BIOS隐藏设置，请使用其他方法(如ru.efi)

-----------------------------------------------------------------------------------------------------
配制提示

1. i7-8550u为Kaby Lake平台
  
2. DVMT修改（以下信息仅供参考，最好自己确认一下，别最后搞的点不亮喽）  
 SaSetup
 区域（area）：0x2
 偏移（offset）：0xDF
 更改：01 to 02
 
3. CFG LOCK（以下信息仅供参考）  
 CpuSetup
 区域（area）：0x3
 偏移（offset）：0x3C
 更改 01 to 00
 
 
-----------------------------------------------------------------------------------------------------
参考内容

1. hojiang23/XiaoxinAir14IKBR_hackintosh   
https://github.com/hojiang23/XiaoxinAir14IKBR_hackintosh/blob/master/README.md

-----------------------------------------------------------------------------------------------------
