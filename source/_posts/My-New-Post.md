---
title: 黑苹果启动参数
date: 2022-01-20 10:15:19
tags:
cover_image: images/wallhaven-nz16pw.png
---
# 黑苹果常见启动参数详解

1. -v ：开启跑马模式，便于从出错的代码中分析故障所在
2. debug=0x100  ：增强-v
3. keepsyms=1 ：增强-v
4. npci=0x2000或npci=0x3000：主板X79、X99、X299 参数修正一些pci错误
5. 加载Applealc.kext驱动可以启用的参数
6. alcid=X（1、2、3、5、7...）：声卡id，此处的优先级最高，比DeviceProperties中要优先
7. 加载whatevergreen.kext驱动可以启用的参数
8. wegnoegpu: 屏蔽独立显卡
9. wegnoigpu ：屏蔽核显
10. agdpmod=pikera：可用于RX5500/5600/5700/6800/6900系列显卡防止启动过程中黑屏
11. igfxonln=1：使用核显输出时强制HDMI/DP始终在线，防止无法唤醒出现黑屏
12. igfxfw=2：强制加载apple GUC固件，一些软件使用核显加速时可以保持核显最高时钟频率运行达到满速效果
13. 加载AirportBrcmFixup.kext驱动可以启用的参数
14. brcmfx-country=XX （US, CN, #a, ...)：强制改变博通无线网卡的国家区域，修正网卡的信道 
15. 双屏幕外接开机主屏幕黑屏：启动参数添加 igfxagdc=0