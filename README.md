# Lenovo-K4350A-Hackintosh
MacOS Mojave/Catalina on Lenovo K4350A Hackintosh
在联想昭阳K4350A上运行黑苹果
#### 本分支仅对Catalina进行支持，其他版本请选择其他分支
## 更新日志
2021-7-7 新增对Catalina的支持
## 电脑配置
| 规格     | 详细信息                                |
| -------- | --------------------------------------- |
| 电脑型号 | 联想 昭阳 K4350A                        |
| 处理器   | Intel(R) Core(TM) i3-3227U CPU @ 1.9GHz |
| 内存     | 8 GB  2400MHz                           |
| 硬盘     | 自带的某东芝500G 5400转的硬盘           |
| 显卡     | Intel HD 4000                           |
| 声卡     | ALC269                                  |
## 正常
1. CPU和核显工作正常
2. USB端口正常
3. 摄像头正常
4. 声卡正常
5. 有线网卡正常
6. 核显硬件加速正常
7. 无线网卡正常
## 未知
1. HDMI是否可以使用
## 不能用的
1. 蓝牙无法使用
2. 睡眠无法使用
3. 屏幕亮度调节无法使用
4. 触摸板无法使用
# 如何安装
1. 克隆本仓库或[下载zip](https://github.com/huangshi10492/Lenovo-K4350A-Hackintosh/archive/master.zip)。
2. 下载10.15镜像并烧写至u盘。
3. 用DiskGenius之类的能读写EFI分区的软件替换EFI文件夹内容。
4. 开干！
# 安装后需要调整的东西
1. 把睡眠时间调成永不。
2. 在Windows下使用apfs读写工具(如apfs for windows)删除 /System/library/Extensions/AppleIntelCPUPowerManagement.kext 、 /System/Library/Extensions/AppleIntelCPUPowerManagementClient.kext 和 /System/Library/Caches/com.apple.kext.caches/Startup ，并将仓库other文件夹下的NullCPUPowerMangement.kext放入/System/library/Extensions中。 [来源](https://blog.csdn.net/u010372981/article/details/81714524)
3. 下载[HeliPort](https://github.com/OpenIntelWireless/HeliPort/releases)来连接wifi。(在EFI/CLOVER文件夹下有)
