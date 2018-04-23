# config eclipse for arm develop

[参考教程](https://mcuoneclipse.com/2017/07/30/breathing-with-oxygen-diy-arm-cortex-m-cc-ide-and-toolchain-with-eclipse-oxygen/)

## basic ide(GNU MCU Eclipse)

1. 下载[Eclipse IDE for C/C++ Developers 64 bit](https://www.eclipse.org/downloads/eclipse-packages/)
1. 解压到`C:\dev\ide\eclipse`
1. 启动`eclipse`，菜单`Window > Preferances`打开全局配置
1. 新出现的`Preferances`窗口左上角`type filter text`处输入`proxy`，点下面加粗的`Network Connections`
1. 右侧`Network Connections`配置页面上部`Active Provider`下拉选择`Manual`
1. 右侧`Network Connections`配置页面中部`Proxy entries`内，双击`HTTP`，新窗口`Host`输入`127.0.0.1`，`Port`输入`1080`，点`OK`结束
1. 右侧`Network Connections`配置页面中部`Proxy entries`内，双击`SOCKS`，新窗口`Host`输入`127.0.0.1`，`Port`输入`1080`，点`OK`结束
1. 右侧`Network Connections`配置页面底部，点`Apply`保存
1. `Preferances`窗口右上角，点`X`关闭窗口

## plugins

> 先安装的插件安装后不要点`Restart`重启，装完最后一个再重启

1. 菜单`Help > Eclipse Marketplace`打开插件市场
1. `Eclipse Marketplace`上部`Find`输入`mcu`，回车执行搜索，窗口中部列表找到`GNU MCU Eclipse`，点`Install`
1. `Find`输入`bracketeer`，回车执行搜索，窗口中部列表找到`Bracketeer for C/C++ (CDT)`，点`Install`
1. `Find`输入`devstyle`，回车执行搜索，窗口中部列表找到`Derkest Dark Theme with DevStyle`，点`Install`

## toolchain

1. 到[这里](https://github.com/gnu-mcu-eclipse/windows-build-tools/releases)下载`make`工具：`gnu-mcu-eclipse-build-tools-2.10-20180103-1919-win64.zip`
1. 解压到`C:\dev\ide\eclipse`
1. 到[这里](https://developer.arm.com/open-source/gnu-toolchain/gnu-rm/downloads)下载`GCC`：`gcc-arm-none-eabi-7-2017-q4-major-win32.zip`
1. 解压到`C:\dev\ide\eclipse\gcc-arm-none-eabi-7-2017-q4-major-win32`
1. 回到`eclipse`，菜单`Window > Preferances`打开全局配置
1. 新出现的`Preferances`窗口左侧列表找到`MCU`，展开，点下面的`Global Build Tools Path`
1. 右侧`Global Build Tools Path`配置页面上部`Build Tools folder`直接输入`${eclipse_home}\GNU MCU Eclipse\Build Tools\2.10-20180103-1919\bin`，配置页面底部，点`Apply`保存
1. `Preferances`窗口右上角，点`X`关闭窗口
1. `Preferances`窗口左侧列表点`Global ARM Toolchains Paths`
1. 右侧`Global ARM Toolchains Paths`配置页面上部`Toolchain folder`直接输入`${eclipse_home}\gcc-arm-none-eabi-7-2017-q4-major-win32\bin`，配置页面底部，点`Apply`保存
1. `Preferances`窗口右上角，点`X`关闭窗口
