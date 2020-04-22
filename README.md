# Linux-based Development
Linux（主要基于Debian系）系统下的开发资料

<br />

- [程序员学习道路第一条，学会Git,一学就会](https://www.toutiao.com/a6694015880218542606)
- [一篇文章，教你学会Git](https://www.toutiao.com/a6774284445873603083/)
- [LinuxVersions](https://kernelnewbies.org/LinuxVersions)
- [Linux 下载文件命令](https://blog.csdn.net/hitabc141592/article/details/7561239)
- [Linux curl命令详解](https://www.cnblogs.com/duhuo/p/5695256.html)
- [Linux下的tar压缩解压缩命令详解](https://www.cnblogs.com/qq78292959/archive/2011/07/06/2099427.html)
- Linux下使用zip来压缩文件夹：`zip -r dst_file.zip src_folder_path`
- [Linux下的mv命令](https://www.cnblogs.com/peida/archive/2012/10/27/2743022.html)
- [vi 常用命令行](https://www.cnblogs.com/sunormoon/archive/2012/02/10/2345326.html)（文件保存退出一般使用`:x`命令）
- [Linux文件查找命令](https://blog.csdn.net/qq_27517377/article/details/78870293)
- [Linux系统下查看文件与磁盘空间大小](https://www.cnblogs.com/adolfmc/archive/2013/02/16/2913801.html)
- [Linux的秘密：这才是find的正确使用姿势](https://www.toutiao.com/i6549496730935624195/)
- [从今往后，谁再告诉你Linux上chmod -R 777解决权限，果断绝交](https://www.toutiao.com/a6811852198561972744/)
- [apt和apt-get之间的区别解释](https://www.toutiao.com/i6734877338686718477/)
- [Sound recording program using Nano](https://raspberrypi.stackexchange.com/questions/15018/sound-recording-program-using-nano)
- [Install alsa-utils on Ubuntu: sudo apt-get install alsa-utils](https://www.devmanuals.net/install/ubuntu/ubuntu-12-04-lts-precise-pangolin/install-alsa-utils.html)
- [Sound Recording & Play on Raspberry Pi Using ALSA in C](https://stackoverflow.com/questions/38615396/sound-recording-play-on-raspberry-pi-using-alsa-in-c)
- [使用ALSA检查声卡驱动](https://www.alsa-project.org/wiki/SoundcardTesting)（在Linux下，**alsamixer** 工具在 `/usr/bin/alsamixer`下，使用F6可切换声卡。也可以使用 `arecord -l` 命令来列出支持麦克风声卡的驱动。）
- [【Linux&音频】Alsa音频编程【精华】](https://www.cnblogs.com/lifan3a/articles/5481993.html)
- [教程】树莓派设置3.5mm接口输出音频](https://www.jianshu.com/p/674145fe98fa)
- [树莓派之蓝牙编程](https://blog.csdn.net/qq_25005909/article/details/77512903)
- [树莓派连接USB转串口的使用](https://blog.csdn.net/fhqlongteng/article/details/80417028)
- [用树莓派玩转蓝牙](https://www.cnblogs.com/vamei/p/6753531.html)
- [树莓派 3B+ 原生蓝牙与手机通讯（BlueTooth SPP）方法和步骤](https://blog.csdn.net/wanyeye/article/details/52909869)
- [Linux(RaspberryPi)上使用BLE低功耗蓝牙](https://blog.csdn.net/qq_33433070/article/details/78668105)
- [Creating BLE GATT Server (UART Service) on Raspberry Pi](https://scribles.net/creating-ble-gatt-server-uart-service-on-raspberry-pi/)
- [Chapter 4. Bluetooth programming in C with BlueZ](https://people.csail.mit.edu/albert/bluez-intro/c404.html)（安装蓝牙开发库：`sudo apt-get install libbluetooth-dev`）
-  [linux Bluetooth programming in c](https://stackoverflow.com/questions/11408609/linux-bluetooth-programming-in-c)
- [Generic Attribute Profile (GATT)](http://dev.ti.com/tirex/content/simplelink_cc2640r2_sdk_1_40_00_45/docs/blestack/ble_user_guide/html/ble-stack-3.x/gatt.html)
- [BLE master/slave, GATT client/server, and data RX/TX basics](https://www.silabs.com/community/wireless/bluetooth/knowledge-base.entry.html/2015/08/06/_reference_ble_mas-gviy)
- 含有调用`hci_le_set_advertise_enable` API的代码必须使用`sudo`来运行，否则会出现“认证失败”的错误码。
- [bleno で Raspberry Pi を BLE Peripheral として動かしてみる](https://qiita.com/comachi/items/c494e0d6c6d1775a3748)
- [Bluetooth GATT: How to Design Custom Services & Characteristics \[MIDI device use case\]](https://www.novelbits.io/bluetooth-gatt-services-characteristics/)
- [串口通讯的原理、代码实现及注释](https://www.toutiao.com/a6729730596051878404)
- [ubuntu安装最新版node和npm](https://www.jianshu.com/p/f2592d106aac)
- [Linux下使用游戏手柄](https://blog.csdn.net/qq_25556149/article/details/79730217)
- [蓝牙hid协议源码解析](https://blog.csdn.net/u012439416/article/details/54348438)
- [gtk 实现键盘按键的读取](https://blog.csdn.net/shibixiao/article/details/4861117)（最后可以将"key-press-event"添加到window对象上以实现全局侦听）
- [GTK进阶学习：鼠标事件](http://www.mamicode.com/info-detail-445416.html)
- [cmake 简介](https://www.cnblogs.com/lidabo/p/7359422.html)
- [cmake构建时指定编译器架构(x86 or x64)](https://www.cnblogs.com/lidabo/p/12017014.html)
- [Android NDK 开发之 CMake 必知必会](https://blog.csdn.net/zhying719/article/details/82657519)
- CMake下开启汇编文件的编译：类Unix下使用GAS为 `ENABLE_LANGUAGE(ASM)`；Visual Studio下使用MASM为 `ENABLE_LANGUAGE(ASM_MASM)`。
- [GNU Make in Detail for Beginners](https://opensourceforu.com/2012/06/gnu-make-in-detail-for-beginners/)
- [linux下的C语言开发（makefile编写详解）](https://www.toutiao.com/i6763898618379239950/)
- 在各类make工具中， **`CC`** 表示C语言编译器， **`CXX`** 表示C++语言编译器。
- [What are the environment variables by default?](https://unix.stackexchange.com/questions/329429/what-are-the-environment-variables-by-default)
- [树莓派Virtual keyboard activation](https://raspberrypi.stackexchange.com/questions/41150/virtual-keyboard-activation)
- [树莓派引脚编号说明](https://www.toutiao.com/a6746428899854385668/)
- Raspbian安装OpenGL ES与EGL：`sudo apt-get install libva-egl1 libegl1-mesa-drivers gegl libgles2-mesa-dev libglfw-dev`
- [Only OpenGL ES 1.1 and not 2.0 on Raspberry Pi 3](https://stackoverflow.com/questions/48136077/only-opengl-es-1-1-and-not-2-0-on-raspberry-pi-3)
- [Raspberry Pi VideoCore APIs](https://elinux.org/Raspberry_Pi_VideoCore_APIs)
- [linux下获取按键响应事件](https://www.cnblogs.com/yangwindsor/articles/3454955.html)（这种方式是阻塞式的）
- [Raspbian下在EGL环境中捕获键盘按键响应事件](https://github.com/AndrewFromMelbourne/raspidmx/blob/master/common/key.c)（Linux下获得鼠标事件可参考Raspbian系统下`/opt/vc/src/hello_pi/hello_triangle2`这一demo。）
- [Linux 下的进程间通信：共享存储](https://www.toutiao.com/a6688140435799409160)
- [共享内存才是实现进程间通信最简单也是最直接的方法](https://www.toutiao.com/a6736813277818389006/)
- [Arm Cortex-M低功耗模式基础](https://www.toutiao.com/a6690433824859357709)
- [Linux内核中的软中断、tasklet和工作队列](http://blog.csdn.net/T146lLa128XX0x/article/details/79070798)
- [How To Install LLVM and Clang on CentOS 6](https://www.vultr.com/docs/how-to-install-llvm-and-clang-on-centos-6)
- [在Centos-5下安装Objective-C的编译环境](http://blog.csdn.net/Robincui2011/article/details/6785987)
- [浅谈 Linux下的零拷贝机制](https://www.toutiao.com/i6462135845481611790/)
- [零拷贝(zero copy)技术你真的懂吗？什么时候需要用到内存映射？](https://www.toutiao.com/a6810663802636337677/)
- [浅谈mmap介绍](https://www.toutiao.com/a6756789193474572808/)
- [聊聊文件IO](https://www.toutiao.com/a6700806648274878987)
- [分钟搞懂Linux中直接I/O原理](https://www.toutiao.com/a6701654059910169091/)
- [高级程序员进阶：了解Linux I/O 调度器，优化系统性能](https://www.toutiao.com/a6735373272432509452/)
- [epoll原理简介](https://www.toutiao.com/a6701457609444033031)
- [如果这篇文章说不清epoll的本质，那就过来掐死我吧！](https://www.toutiao.com/a6683264188661367309)
- [非阻塞 I/O 和多路复用+select、poll、epoll模型详解](https://www.toutiao.com/i6554223409138500110)
- [io_submit：Linux内核新加入的epoll替代方案](https://www.toutiao.com/a6809889593286984206/)
- [kqueue用法简介](https://www.cnblogs.com/luminocean/p/5631336.html)
- [使用 kqueue 在 FreeBSD 上开发高性能应用服务器](https://www.ibm.com/developerworks/cn/aix/library/1105_huangrg_kqueue/)
- [使程序在Linux下后台运行 （关掉终端继续让程序运行的方法）](https://www.cnblogs.com/little-ant/p/3952424.html)
- Linux下生成动态库使用` -fPIC -shared`编译选项，并且动态库的命名规则为：lib<lib-name>.so。加载动态库时使用`export LD_LIBRARY_PATH=`导出动态库所在路径。
- [Memory Allocation Guide](https://www.kernel.org/doc/html/latest/core-api/memory-allocation.html)
- [Linux系统监控：虚拟内存](https://www.cnblogs.com/luoahong/articles/7911266.html)
- [linux虚拟内存，内存及内存管理相关](https://blog.csdn.net/chen_jianjian/article/details/88876392)
- [Linux内核Page Cache和Buffer Cache关系及演化历史](https://www.toutiao.com/a6816861382776979976/)
- [Linux内核快速处理路径尽量多用slab而慎用kmalloc](https://blog.csdn.net/dog250/article/details/105544111)
- GAS下使用Intel语法汇编并且在寄存器前不添加`%`符号：`.intel_syntax noprefix`。
- GCC/Clang编译器下要使用<intrin.h>，则得：`#include <x86intrin.h>`。
- [How do I call “cpuid” in Linux?](https://stackoverflow.com/questions/14266772/how-do-i-call-cpuid-in-linux)
- [Linux 获取本机IP、MAC地址用法大全](https://www.cnblogs.com/fnlingnzb-learner/p/6427786.html)
- [C++ win32和linux获取系统剩余内存](https://blog.csdn.net/q1368232592/article/details/85157823)
- [Linux下获取内核版本号的函数](https://blog.csdn.net/ly890700/article/details/53540653)
- [Linux查看物理CPU个数、核数、逻辑CPU个数](https://www.cnblogs.com/bugutian/p/6138880.html)
- [Linux如何查看CPU信息，Linux查看CPU个数和核心数，Linux查看CPU使用率和运行位数](https://blog.csdn.net/tiiefu1212/article/details/78623132)
- [教你写第一个Linux设备驱动程序](https://www.toutiao.com/a6812972562201444878/)
- [Ubuntu系统下通过Clang编译器编写Objective-C](https://blog.csdn.net/zenny_chen/article/details/52507022)
- Ubuntu下安装libz库：`sudo apt-get install zlib1g-dev`，然后使用`-lz`去连接。
- Ubuntu下安装BSD库：`sudo apt-get install libbsd-dev`，然后使用`-lbsd`去连接。此外，在`<bsd/stdlib.h>`中可使用 **arc4random** 等函数。
- Ubuntu下安装glib库：`sudo apt-get install libglib2.0-dev`。主要头文件为：`<glib.h>`。使用`pkg-config --cflags glib-2.0`可观察详细编译选项；使用`pkg-config --libs glib-2.0`可详细查看需要连接的库。如果我们要使用gobject库，那么将上述查看编译和连接选项的库名改为`gobject-2.0`即可。gobject库的头文件为：`<glib-object.h>`。
- [GLib开源项目](https://gitlab.gnome.org/GNOME/glib)
- Ubuntu下查看当前所有可安装的软件包：`dpkg -l`。
- [Download C# Mono](https://www.mono-project.com/download/stable/#download-lin)（安装完整的Mono：`sudo apt-get install mono-complete`。安装Monodevelop IDE：`sudo apt-get install monodevelop`。不过在树莓派上无法安装Monodevelop IDE，因此直接编译C#代码使用`mcs`命令，可直接生成可执行代码。对于mcs命令，使用`-unsafe`选项可启用非安全代码。）
- [.net、mono和C#](https://www.cnblogs.com/kekec/p/7237156.html)
- [人工智能开发必须掌握的那些Linux指令（基础篇）](https://mp.weixin.qq.com/s?srcid=&scene=23&sharer_sharetime=1587431414733&mid=2651236909&sharer_shareid=c0f8ad645f1b221a7a43ae65e09fb2ea&sn=77d6eccac6e96b97e3c5d18d1665eef2&idx=2&__biz=MjM5NTE3Nzk4MQ%3D%3D&chksm=bd0e7ebf8a79f7a98ff345c7054cabc816a07a69073401f75d874f7d571e8d2f310da0bf4a9f&mpshare=1#rd)
- [人工智能开发必须掌握的那些Linux指令（进阶篇）](https://mp.weixin.qq.com/s?srcid=&scene=23&sharer_sharetime=1587524349426&mid=2651236928&sharer_shareid=c0f8ad645f1b221a7a43ae65e09fb2ea&sn=f4744d4801f7edfebe40717101799849&idx=1&__biz=MjM5NTE3Nzk4MQ%3D%3D&chksm=bd0e7ed28a79f7c47fc635600df7f7a5fde900de2fa8bb0884cd9badb3a4af6d6445e9d3a1bf&mpshare=1#rd)

<br/>

如果在Ubuntu上安装GCC或使用`sudo apt-get install build-essential`失败，则需要先执行一下`sudo apt-get update`，更新之后再执行安装命令。

<br />

## Raspbian系统下所需要安装的开发工具
```bash
sudo apt-get update

sudo apt-get install build-essential

# 安装用于Objective-C的GNUstep
sudo apt-get install gnustep
sudo apt-get install gnustep-devel

# 安装GTK+3
sudo apt-get install libgtk-3-dev

# 安装asound2库
sudo apt-get install libasound2-dev

# 安装alsa-utils
sudo apt-get install alsa-utils

# 安装蓝牙相关工具
sudo apt-get install blueman

# 安装bluetooth开发库
sudo apt-get install libbluetooth-dev

```

<br />

## GNUstep编译选项

我们通过执行以下命令来观察Objective-C编译时所需要的编译选项：`gnustep-config --objc-flags`    
执行以下命令查看Objective-C连接时所需要的加载选项：`gnustep-config --objc-libs`

整理之后：
```bash
export GCC_PATH=/usr/lib/gcc/arm-linux-gnueabihf/8/
gcc test.m -std=gnu11 -Os  -MMD -MP -DGNUSTEP -DGNUSTEP_BASE_LIBRARY=1 -DGNU_RUNTIME=1 -DGNUSTEP_BASE_LIBRARY=1 -fno-strict-aliasing -pthread -fPIC -Wall -DGSWARN -DGSDIAGNOSE -Wno-import -fgnu-runtime -fconstant-string-class=NSConstantString  -I. -I/usr/local/include/GNUstep -I/usr/include/GNUstep -I${GCC_PATH}include/  -rdynamic -L/root/GNUstep/Library/Libraries -L/usr/local/lib -L/usr/lib -lobjc -lm -lgnustep-base -o test
```

<br />

## GTK+ 3编译选项

查看当前环境的GTK+ 3编译选项：`pkg-config --cflags --libs gtk+-3.0`


整理之后：
```bash
export ABI_NAME=${HOSTTYPE}-${OSTYPE}
gcc main.c -std=gnu11 -I/usr/include/glib-2.0/ -I/usr/include/atk-1.0/ -I/usr/include/gdk-pixbuf-2.0/ -I/usr/include/cairo/ -I/usr/include/pango-1.0/ -I/usr/lib/${ABI_NAME}/glib-2.0/include/ -I/usr/include/gtk-3.0/ -L/usr/lib/${ABI_NAME}/ -lgtk-3 -lgobject-2.0 -lpangocairo-1.0 -lgio-2.0 -latk-1.0 -lgdk-3 -lglib-2.0    -o gtk-test
```

<br />

### 安装LLVM-Clang

```shell
sudo apt-get install llvm

sudo apt-get install clang

sudo apt-get install libdispatch-dev
```
从GCC 8起，Clang 6起可以使用`-std=gnu17`标准。

<br />

### C语言中，在控制台中读取一行输入命令字符串

```c
    char *contents = NULL;
    size_t initLen = 0;
    // contents最后会包含一个换行符，这也就是意味着如果用户仅输入一个回车，
    // 那么contents中就一个换行符，长度为1。
    ssize_t contentLength = getline(&contents, &initLen, stdin);
    printf("Content length is: %zd, content is: %s", contentLength, contents);
```
以上代码只需要包含`<stdio.h>`头文件即可。这里需要注意的是，getline的第二个参数不能为空。

<br />

