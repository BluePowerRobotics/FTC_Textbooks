## 1. ADB（Android Debug Bridge）概述

### a) 简介
ADB 是 Android SDK 中的命令行工具，用于与 Android 设备通信并执行调试功能，包含以下组件：
- **客户端**：通过命令行调用的程序  
- **服务器**：管理客户端与设备间的通信  
- **守护进程 (adbd)**：运行在设备上执行命令  

### b) 安装 & 启动
1. 下载 Android SDK Platform Tools：
   - 前往 [https://dl.google.com/android/repository/platform-tools-latest-windows.zip](https://dl.google.com/android/repository/platform-tools-latest-windows.zip) 下载。
2. 配置环境变量：
   - 将解压后的 `platform-tools` 目录添加到系统 `PATH` 中。
3. 设备端配置：
   - 在 Android 设备上启用开发者模式，并打开 USB 调试。

### c) 用法

#### i. 设备管理
```bash
# 列出连接的设备
adb devices

# 连接无线设备
adb connect <IP:端口>

# 断开设备
adb disconnect
```

#### ii. 应用管理
```bash
# 安装 APK
adb install [选项] <本地路径.apk>
# 示例：-r 覆盖安装，-s 安装到 SD 卡

# 卸载应用
adb uninstall <包名>

# 启动应用
adb shell am start -n <包名/活动名>
```

#### iii. 文件操作
```bash
# 推送文件到设备
adb push <本地路径> <设备路径>

# 从设备拉取文件
adb pull <设备路径> <本地路径>
```

#### iv. 调试 & 日志
```bash
# 查看设备日志（支持过滤）
adb logcat [-s TAG] [-c 清空日志]

# 进入设备 Shell
adb shell
```

#### v. 系统操作
```bash
# 重启设备（可选 recovery/bootloader 模式）
adb reboot [选项]

# 截图
adb shell screencap <设备文件路径>

# 录屏
adb shell screenrecord <设备文件路径>

# 备份与恢复
adb backup -apk -shared -all -f backup.ab
adb restore backup.ab
```

#### vi. 权限管理
```bash
# 获取 root 权限
adb root

# 挂载系统分区为可写
adb remount
```

#### vii. Shell 子命令
```bash
# 包管理
pm list packages
pm path <包名>

# 强制停止应用
am force-stop <包名>
```

#### viii. 其他
```bash
# 启用无线 ADB
adb tcpip <端口>

# 查看帮助
adb -help
```

### d) 练习
> **问题**：已通过有线连接 Android 设备，如何启用无线 ADB 连接？  
> **答案**：  
> 1. `adb tcpip 5555`  
> 2. `adb connect <Android设备IP>:5555`  
