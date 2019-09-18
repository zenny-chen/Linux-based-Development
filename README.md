# Linux-based-Development
Linux（主要基于Debian系）系统下的开发资料

<br />

1. [程序员学习道路第一条，学会Git,一学就会](https://www.toutiao.com/a6694015880218542606)
1. [Sound recording program using Nano](https://raspberrypi.stackexchange.com/questions/15018/sound-recording-program-using-nano)
1. [Install alsa-utils on Ubuntu: sudo apt-get install alsa-utils](https://www.devmanuals.net/install/ubuntu/ubuntu-12-04-lts-precise-pangolin/install-alsa-utils.html)
1. [Sound Recording & Play on Raspberry Pi Using ALSA in C](https://stackoverflow.com/questions/38615396/sound-recording-play-on-raspberry-pi-using-alsa-in-c)
1. [使用ALSA检查声卡驱动](https://www.alsa-project.org/wiki/SoundcardTesting)（在Linux下，**alsamixer** 工具在 `/usr/bin/alsamixer`下，使用F6可切换声卡。也可以使用 `arecord -l` 命令来列出支持麦克风声卡的驱动。）
1. [【Linux&音频】Alsa音频编程【精华】](https://www.cnblogs.com/lifan3a/articles/5481993.html)
1. [教程】树莓派设置3.5mm接口输出音频](https://www.jianshu.com/p/674145fe98fa)
1. [树莓派之蓝牙编程](https://blog.csdn.net/qq_25005909/article/details/77512903)
1. [树莓派连接USB转串口的使用](https://blog.csdn.net/fhqlongteng/article/details/80417028)
1. [用树莓派玩转蓝牙](https://www.cnblogs.com/vamei/p/6753531.html)
1. [树莓派 3B+ 原生蓝牙与手机通讯（BlueTooth SPP）方法和步骤](https://blog.csdn.net/wanyeye/article/details/52909869)
1. [Linux(RaspberryPi)上使用BLE低功耗蓝牙](https://blog.csdn.net/qq_33433070/article/details/78668105)
1. [Creating BLE GATT Server (UART Service) on Raspberry Pi](https://scribles.net/creating-ble-gatt-server-uart-service-on-raspberry-pi/)
1. [Chapter 4. Bluetooth programming in C with BlueZ](https://people.csail.mit.edu/albert/bluez-intro/c404.html)（安装蓝牙开发库：`sudo apt-get install libbluetooth-dev`）
1.  [linux Bluetooth programming in c](https://stackoverflow.com/questions/11408609/linux-bluetooth-programming-in-c)
1. [Generic Attribute Profile (GATT)](http://dev.ti.com/tirex/content/simplelink_cc2640r2_sdk_1_40_00_45/docs/blestack/ble_user_guide/html/ble-stack-3.x/gatt.html)
1. [BLE master/slave, GATT client/server, and data RX/TX basics](https://www.silabs.com/community/wireless/bluetooth/knowledge-base.entry.html/2015/08/06/_reference_ble_mas-gviy)
1. 含有调用`hci_le_set_advertise_enable` API的代码必须使用`sudo`来运行，否则会出现“认证失败”的错误码。
1. [bleno で Raspberry Pi を BLE Peripheral として動かしてみる](https://qiita.com/comachi/items/c494e0d6c6d1775a3748)
1. [Bluetooth GATT: How to Design Custom Services & Characteristics \[MIDI device use case\]](https://www.novelbits.io/bluetooth-gatt-services-characteristics/)
1. [串口通讯的原理、代码实现及注释](https://www.toutiao.com/a6729730596051878404)
1. [ubuntu安装最新版node和npm](https://www.jianshu.com/p/f2592d106aac)
1. [Linux下使用游戏手柄](https://blog.csdn.net/qq_25556149/article/details/79730217)
1. [蓝牙hid协议源码解析](https://blog.csdn.net/u012439416/article/details/54348438)
1. [gtk 实现键盘按键的读取](https://blog.csdn.net/shibixiao/article/details/4861117)（最后可以将"key-press-event"添加到window对象上以实现全局侦听）
1. [GTK进阶学习：鼠标事件](http://www.mamicode.com/info-detail-445416.html)
1. [cmake 简介](https://www.cnblogs.com/lidabo/p/7359422.html)
1. [Android NDK 开发之 CMake 必知必会](https://blog.csdn.net/zhying719/article/details/82657519)
1. 在各类make工具中， **`CC`** 表示C语言编译器， **`CXX`** 表示C++语言编译器。
1. [What are the environment variables by default?](https://unix.stackexchange.com/questions/329429/what-are-the-environment-variables-by-default)
1. [树莓派Virtual keyboard activation](https://raspberrypi.stackexchange.com/questions/41150/virtual-keyboard-activation)
1. Raspbian安装OpenGL ES与EGL：`sudo apt-get install libva-egl1 libegl1-mesa-drivers gegl libgles2-mesa-dev libglfw-dev`
1. [Only OpenGL ES 1.1 and not 2.0 on Raspberry Pi 3](https://stackoverflow.com/questions/48136077/only-opengl-es-1-1-and-not-2-0-on-raspberry-pi-3)
1. [Raspberry Pi VideoCore APIs](https://elinux.org/Raspberry_Pi_VideoCore_APIs)
1. [linux下获取按键响应事件](https://www.cnblogs.com/yangwindsor/articles/3454955.html)（这种方式是阻塞式的）
1. [Raspbian下在EGL环境中捕获键盘按键响应事件](https://github.com/AndrewFromMelbourne/raspidmx/blob/master/common/key.c)（Linux下获得鼠标事件可参考Raspbian系统下`/opt/vc/src/hello_pi/hello_triangle2`这一demo。）
1. [Linux 下的进程间通信：共享存储](https://www.toutiao.com/a6688140435799409160)
1. [Linux 获取本机IP、MAC地址用法大全](https://www.cnblogs.com/fnlingnzb-learner/p/6427786.html)
1. [Arm Cortex-M低功耗模式基础](https://www.toutiao.com/a6690433824859357709)
1. [类Unix系统中如何获取另一个程序的输出内容](https://baike.baidu.com/item/popen)
1. [使用popen执行shell命令并获取返回结果](https://www.cnblogs.com/hiawind/p/9089288.html)
1. [C语言中的系统库system函数](https://baike.baidu.com/item/system/15078602?fr=aladdin)
1. [gdb到底是怎样实现的？](https://www.toutiao.com/a6699652803918299655)
1. [聊聊文件IO](https://www.toutiao.com/a6700806648274878987)
1. [epoll原理简介](https://www.toutiao.com/a6701457609444033031)
1. [分钟搞懂Linux中直接I/O原理](https://www.toutiao.com/a6701654059910169091/)

<br/>

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

