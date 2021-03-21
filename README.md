# Lenovo-K4350A-Hackintosh

MacOS Mojave on Lenovo K4350A Hackintosh
在联想昭阳K4350A上运行黑苹果
基于[黑果小兵的镜像macOS Mojave 10.14.6(18G103) Installer for Intel and AMD with Clover 5091 and WEPE.dmg](https://mirrors.dtops.cc/iso/MacOS/daliansky_macos/10.14/)
在此感谢 👍

## 只搞了一点，处于基本能用的级别

# 电脑配置

|规格|详细信息|
|---|---|
|电脑型号|联想 昭阳 K4350A|
|操作系统|macOS Mojave 10.14.6(18G103)|
|处理器|Intel(R) Core(TM) i3-3227U CPU @ 1.9GHz|
|内存|8 GB  2400MHz|
|硬盘|自带的某东芝500G 5400转的硬盘|
|显卡|Intel HD 4000|
|声卡|ALC269|

## 本人还是一个新手，如果有什么错误请指正

# 正常
1. cpu和核显工作正常
2. USB端口正常
3. 触摸板正常
4. 摄像头正常
5. 电脑屏幕能亮 
6. 有线网卡正常
7. 核显有硬件加速(应该)
# 未知
1. 不知道HDMI能不能用
2. 不知道内置的麦克风能不能用(应该是不能的)
3. 不知道电池正不正常(我是把它当作台式用的)
4. 不知道独立显卡屏蔽了没
5. 不知道cpu有没有变频
# 不能用的
1. 蓝牙不能用(主要是懒)
2. 无线网卡不能用
3. 睡眠不能用(直接就睡死了)
# 不完善的
1. 声卡用的是万能驱动，需要手动切换扬声器和耳机，有时候通知没有声音。
2. 屏幕亮度的调节幅度有点小，晚上看可能会瞎。

# 我是怎么处理一些问题的
1. 网卡我用了一个TP-Lnk的无线网卡，在TP的国外官网下的Mac驱动居然可以用，但是用的是TP自己的网络管理。
2. 屏幕太亮我找了个护眼软件开夜间模式解决。

# 如何安装
1. 克隆本仓库或[下载zip](https://github.com/huangshi10492/Lenovo-K4350A-Hackintosh/archive/master.zip)。
2. 根据[黑果小兵的教程](https://blog.daliansky.net/macOS-Mojave-10.14.6-18G87-Release-version-with-Clover-5033-original-image.html)把镜像装到u盘上。
3. 用DiskGenius之类的能读写EFI分区的软件把EFI文件夹下的CLOVER删掉换成我提供的。
4. 开干！

# 安装后需要调整的东西
1. 把睡眠时间调成永不。
2. 看看声音的输出有没有问题。
3. 修改调节亮度的快捷键(不支持Fn键调节)。
4. (重要)在Windows下使用apfs读写工具(如apfs for windows)删除 /System/library/Extensions/AppleIntelCPUPowerManagement.kext 、 /System/Library/Extensions/AppleIntelCPUPowerManagementClient.kext 和 /System/Library/Caches/com.apple.kext.caches/Startup ，并将仓库other文件夹下的NullCPUPowerMangement.kext放入/System/library/Extensions中。 [来源](https://blog.csdn.net/u010372981/article/details/81714524)
