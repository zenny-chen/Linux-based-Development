# Linux-based Development
Linux（主要基于Debian系）系统下的开发资料

<br />

- [GitLab CI Pipeline Stage Timeout](https://stackoverflow.com/questions/38403681/gitlab-ci-pipeline-stage-timeout)
- [GitLab CI/CD Set job start timeout](https://forum.gitlab.com/t/set-job-start-timeout/34993)
- [LinuxVersions](https://kernelnewbies.org/LinuxVersions)
- Linux显示当前目录的 **绝对路径** 命令：**`pwd`**。
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
- [Linux创建快捷方式的几种方法](https://blog.csdn.net/qq_41115033/article/details/123829766)（通常使用这种方式：**`sudo ln -s /opt/lib/libapp.so.6  /usr/lib/libapp.so`**）
- [linux拷贝软连接文件](https://www.cnblogs.com/macrored/p/11753862.html)（拷贝含有软链接文件的文件夹，可以使用 **`-frL`**，使得里面所有的软链接文件变成独立的它原本所链接到的目标文件的拷贝。通常用这种方式可以将包含软链接文件的文件夹拷贝到网盘、U盘等其他存储介质。）
- [Ubuntu下如何用命令行运行deb安装包](https://blog.csdn.net/xxdw1992/article/details/124816245)
- [漫画 | Unix/Linux 比 Windows 差远了](https://www.toutiao.com/i7044022091791729182/)
- [apt和apt-get之间的区别解释](https://www.toutiao.com/i6734877338686718477/)
- [Linux上如何执行java程序](https://www.cnblogs.com/wanglin2016/p/6013010.html)
- Linux中冒号 **:** 用于分隔路径，点号 **.** 表示当前目录，比如：
```bash
export PATH=$JAVA_HOME/bin:$PATH
export CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
```
- [（超详细）Linux Shell 编程](https://blog.csdn.net/qq_50685659/article/details/125738428)
- [linux常见系统环境变量](https://www.cnblogs.com/renping/p/7020354.html)
- [linux c 编程 环境变量的操作函数](https://blog.csdn.net/q435201823/article/details/107163816)
- [Linux连不上网解决](https://www.cnblogs.com/lbky/articles/11023246.html)
- [Linux下实时查看GPU状态](https://blog.csdn.net/zhang_yang_43/article/details/78357458)
- [A Step-By-Step Guide To Install CMake On Linux](https://www.linuxfordevices.com/tutorials/install-cmake-on-linux)（Linux系统安装 **CMake** 的关键命令：**`sudo sh cmake.sh --prefix=/usr/local/ --exclude-subdir`**。The above command will install cmake globally for all users to **`/usr/local/bin`** and the **`--exclude-subdir`** option is to get rid of the extra directory that is produced while extracting the .tar.gz archive.）
- [Linux（centos）下卸载及安装cmake详细步骤](https://blog.csdn.net/qq_22159287/article/details/121916753)
- [linux下卸载旧版本cmake安装新版本cmake](https://blog.csdn.net/qq_40164094/article/details/120196560)
- [Sound recording program using Nano](https://raspberrypi.stackexchange.com/questions/15018/sound-recording-program-using-nano)
- [Install alsa-utils on Ubuntu: sudo apt-get install alsa-utils](https://www.devmanuals.net/install/ubuntu/ubuntu-12-04-lts-precise-pangolin/install-alsa-utils.html)
- [Sound Recording & Play on Raspberry Pi Using ALSA in C](https://stackoverflow.com/questions/38615396/sound-recording-play-on-raspberry-pi-using-alsa-in-c)
- [使用ALSA检查声卡驱动](https://www.alsa-project.org/wiki/SoundcardTesting)（在Linux下，**alsamixer** 工具在 `/usr/bin/alsamixer`下，使用F6可切换声卡。也可以使用 `arecord -l` 命令来列出支持麦克风声卡的驱动。）
- [【Linux&音频】Alsa音频编程【精华】](https://www.cnblogs.com/lifan3a/articles/5481993.html)
- [教程】树莓派设置3.5mm接口输出音频](https://www.jianshu.com/p/674145fe98fa)
- [树莓派更换软件源](https://www.toutiao.com/a6796581937096950283/)
- [树莓派搭建视频监控平台](https://www.toutiao.com/a6847285154025570829/)
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
- 含有调用`hci_le_set_advertise_enable` How do I set a software breakpoint on an ARM processor?API的代码必须使用`sudo`来运行，否则会出现“认证失败”的错误码。
- [bleno で Raspberry Pi を BLE Peripheral として動かしてみる](https://qiita.com/comachi/items/c494e0d6c6d1775a3748)
- [Bluetooth GATT: How to Design Custom Services & Characteristics \[MIDI device use case\]](https://www.novelbits.io/bluetooth-gatt-services-characteristics/)
- [串口通讯的原理、代码实现及注释](https://www.toutiao.com/a6729730596051878404)
- [ubuntu安装最新版node和npm](https://www.jianshu.com/p/f2592d106aac)
- [Linux下使用游戏手柄](https://blog.csdn.net/qq_25556149/article/details/79730217)
- [蓝牙hid协议源码解析](https://blog.csdn.net/u012439416/article/details/54348438)
- [gtk 实现键盘按键的读取](https://blog.csdn.net/shibixiao/article/details/4861117)（最后可以将"key-press-event"添加到window对象上以实现全局侦听）
- [GTK进阶学习：鼠标事件](http://www.mamicode.com/info-detail-445416.html)
- [What are the environment variables by default?](https://unix.stackexchange.com/questions/329429/what-are-the-environment-variables-by-default)
- [树莓派Virtual keyboard activation](https://raspberrypi.stackexchange.com/questions/41150/virtual-keyboard-activation)
- [树莓派引脚编号说明](https://www.toutiao.com/a6746428899854385668/)
- Raspbian安装OpenGL ES与EGL：`sudo apt-get install libva-egl1 libegl1-mesa-drivers gegl libgles2-mesa-dev libglfw-dev`
- [Only OpenGL ES 1.1 and not 2.0 on Raspberry Pi 3](https://stackoverflow.com/questions/48136077/only-opengl-es-1-1-and-not-2-0-on-raspberry-pi-3)
- [Raspberry Pi VideoCore APIs](https://elinux.org/Raspberry_Pi_VideoCore_APIs)
- [linux下获取按键响应事件](https://www.cnblogs.com/yangwindsor/articles/3454955.html)（这种方式是阻塞式的）
- [Raspbian下在EGL环境中捕获键盘按键响应事件](https://github.com/AndrewFromMelbourne/raspidmx/blob/master/common/key.c)（Linux下获得鼠标事件可参考Raspbian系统下`/opt/vc/src/hello_pi/hello_triangle2`这一demo。）
- [Linux下的进程间通信：共享存储](https://www.toutiao.com/a6688140435799409160)
- [共享内存才是实现进程间通信最简单也是最直接的方法](https://www.toutiao.com/a6736813277818389006/)
- [Linux共享内存使用常见陷阱与分析](https://zhuanlan.zhihu.com/p/260418383)
- [Linux内核中的软中断、tasklet和工作队列](http://blog.csdn.net/T146lLa128XX0x/article/details/79070798)
- [多线程 or 多进程？](https://blog.csdn.net/zy799894671/article/details/18405033)
- [Linux内核如何替换内核函数并调用原始函数](https://blog.csdn.net/dog250/article/details/84201114)
- [怎样Hack Linux的内核符号？](https://blog.csdn.net/sinat_30551659/article/details/107705842)
- [How To Install LLVM and Clang on CentOS 6](https://www.vultr.com/docs/how-to-install-llvm-and-clang-on-centos-6)
- [在Centos-5下安装Objective-C的编译环境](http://blog.csdn.net/Robincui2011/article/details/6785987)
- [浅谈 Linux下的零拷贝机制](https://www.toutiao.com/i6462135845481611790/)
- [零拷贝(zero copy)技术你真的懂吗？什么时候需要用到内存映射？](https://www.toutiao.com/a6810663802636337677/)
- [Linux——sendfile零拷贝高效率发送文件](https://blog.csdn.net/lemonchi/article/details/81484152)。sendfile高效传输文件，无需内核态到用户态，用户态到内核态copy数据。
```c
/**
NAME
       sendfile - transfer data between file descriptors

SYNOPSIS
       #include <sys/sendfile.h>
*/
       ssize_t sendfile(int out_fd, int in_fd, off_t *offset, size_t count);
```
- [浅谈mmap介绍](https://www.toutiao.com/a6756789193474572808/)
- [linux库函数mmap\(\)原理及用法详解](https://blog.csdn.net/qq_41687938/article/details/119901916)
- [在Linux中利用mmap模拟Windows的VirtualAlloc](https://blog.csdn.net/cjfeii/article/details/9122279)
- [深入理解 Linux 内核--jemalloc 引起的 TLB shootdown 及优化](https://www.toutiao.com/a6801053138380915211/)
- [Memory Allocation Guide](https://www.kernel.org/doc/html/latest/core-api/memory-allocation.html)
- [Linux系统监控：虚拟内存](https://www.cnblogs.com/luoahong/articles/7911266.html)
- [linux虚拟内存，内存及内存管理相关](https://blog.csdn.net/chen_jianjian/article/details/88876392)
- [万字长文，别再说你不懂Linux内存管理了（合辑），30 张图给你安排的明明白白](https://mp.weixin.qq.com/s?__biz=MzI3ODQ3OTczMw==&mid=2247493251&idx=1&sn=10d495947c4849c6cf854b15e7f6e7c5&chksm=eb54f099dc23798fce0f5db05e080bb0830133504dcfed325c66c2dcae6f4176b36484225676&mpshare=1&scene=23&srcid=01094DqUSLSGFRKOOLtfpqsU)
- [深入理解glibc malloc：malloc() 与 free() 原理图解](https://www.toutiao.com/i7046286983177470500/)
- [Memory Allocation Hooks](https://www.gnu.org/software/libc/manual/html_node/Hooks-for-Malloc.html)（要连接的动态库为：**`libc_malloc_debug.so`**，详细可见：[Securing malloc in glibc: Why malloc hooks had to go](https://developers.redhat.com/articles/2021/08/25/securing-malloc-glibc-why-malloc-hooks-had-go)）
- [Linux内核Page Cache和Buffer Cache关系及演化历史](https://www.toutiao.com/a6816861382776979976/)
- [DMA，Direct IO和零拷贝](https://www.toutiao.com/i6945819523622666782/)
- [Linux内核快速处理路径尽量多用slab而慎用kmalloc](https://blog.csdn.net/dog250/article/details/105544111)
- [聊聊文件IO](https://www.toutiao.com/a6700806648274878987)
- [存储进阶：怎么才能保证 IO 数据的安全？](https://www.toutiao.com/i6959376691781190151/)
- [分钟搞懂Linux中直接I/O原理](https://www.toutiao.com/a6701654059910169091/)
- [高级程序员进阶：了解Linux I/O 调度器，优化系统性能](https://www.toutiao.com/a6735373272432509452/)
- [epoll原理简介](https://www.toutiao.com/a6701457609444033031)
- [如果这篇文章说不清epoll的本质，那就过来掐死我吧！](https://www.toutiao.com/a6683264188661367309)
- [高并发高吞吐IO秘密武器——epoll池化技术](https://www.toutiao.com/i7008441343617794563/)
- [6种epoll的设计，让你吊打面试官，而且他不能还嘴](https://www.toutiao.com/i7009187407606088223/)
- [非阻塞 I/O 和多路复用+select、poll、epoll模型详解](https://www.toutiao.com/i6554223409138500110)
- [io_submit：Linux内核新加入的epoll替代方案](https://www.toutiao.com/a6809889593286984206/)
- [AIO 的新归宿：io_uring](https://zhuanlan.zhihu.com/p/62682475)
- [io_uring只适用于存储IO？大错特错](https://www.toutiao.com/i6884987457641644551/)
- [io_uring vs epoll，谁在网络编程领域更胜一筹？](https://www.toutiao.com/i7045101452641124877/)
- [Linux下全新的异步I/O：io_uring详解](https://www.toutiao.com/i7011043732220805668/)
- [linux异步IO编程实例分析](https://www.toutiao.com/a6875582313590325774/)
- [kqueue用法简介](https://www.cnblogs.com/luminocean/p/5631336.html)
- [使用kqueue在FreeBSD上开发高性能应用服务器](http://www.ibm.com/developerworks/cn/aix/library/1105_huangrg_kqueue/)
- [Linux AIO 异步读写](https://www.cnblogs.com/standardzero/p/12552642.html)
- [最专业的对“鸿蒙”的分析](https://www.toutiao.com/a7039879650885222951/)
- [使程序在Linux下后台运行 （关掉终端继续让程序运行的方法）](https://www.cnblogs.com/little-ant/p/3952424.html)
- Linux下生成动态库使用` -fPIC -shared`编译选项，并且动态库的命名规则为：lib<lib-name>.so。加载动态库时使用`export LD_LIBRARY_PATH=`导出动态库所在路径。
- GCC默认连接静态库使用此连接选项：`-static`。
- GAS下使用Intel语法汇编并且在寄存器前不添加`%`符号：`.intel_syntax noprefix`。
- GCC/Clang编译器下要使用<intrin.h>，则得：`#include <x86intrin.h>`。
- [version 'GLIBC_2.34' not found简单有效解决方法](https://blog.csdn.net/huazhang_001/article/details/128828999)
- [linux中的ld命令及其搜索路径顺序](https://blog.csdn.net/qq_42731705/article/details/123934842)
- [linux下动态库链接静态库问题记录](https://blog.csdn.net/hong_yu0315/article/details/128077943) —— 主要是以下这段：
> msvc系列编译器会将静态库链接到动态库中去，但是在linux系统下，gcc系列编译器并不会将静态库链接至动态库中，gcc仅仅是编译了插件动态库，并没有去链接。

- [How do I call “cpuid” in Linux?](https://stackoverflow.com/questions/14266772/how-do-i-call-cpuid-in-linux)
- [linux下常用的几个时间函数：gettimeofday和clock_gettime](https://blog.csdn.net/fchyang/article/details/81166470)（使用精确时间戳，直接使用`clock_gettime(CLOCK_MONOTONIC, &timespec);`。）
- [Linux下的sleep()和usleep()的使用和区别](https://www.cnblogs.com/ZhaoxiCheung/p/6792734.html)
- [Linux 获取本机IP、MAC地址用法大全](https://www.cnblogs.com/fnlingnzb-learner/p/6427786.html)
- [C++ win32和linux获取系统剩余内存](https://blog.csdn.net/q1368232592/article/details/85157823)
- Linux获取当前系统分发版本信息：`cat /etc/os-release`
- [Linux下获取内核版本号的函数](https://blog.csdn.net/ly890700/article/details/53540653)
- [Linux系统调用--uname()函数及系统下的uname命令](http://blog.chinaunix.net/uid-8996150-id-2011653.html)
- [Linux查看物理CPU个数、核数、逻辑CPU个数](https://www.cnblogs.com/bugutian/p/6138880.html)
- [Linux如何查看CPU信息，Linux查看CPU个数和核心数，Linux查看CPU使用率和运行位数](https://blog.csdn.net/tiiefu1212/article/details/78623132)
- [Linux Shell脚本中获取本机ip地址方法](https://www.cnblogs.com/lidabo/p/15926304.html)
- [获取SYSTEM()执行结果](https://blog.csdn.net/u013625451/article/details/78830104)
- [linux中open()函数的mode_t 含义](https://blog.csdn.net/sdhgood/article/details/39555311)（**`O_LARGEFILE`** 标志用于指示`off_t`无法容下文件大小而只能用`off64_t`）
- [教你写第一个Linux设备驱动程序](https://www.toutiao.com/a6812972562201444878/)
- [How do I set a software breakpoint on an ARM processor?](https://stackoverflow.com/questions/11345371/how-do-i-set-a-software-breakpoint-on-an-arm-processor)
- 对于不支持硬件断点的ARM Linux可使用`raise(SIGTRAP)`系统调用来触发gdb的断点调试。
- [Ubuntu系统下通过Clang编译器编写Objective-C](https://blog.csdn.net/zenny_chen/article/details/52507022)
- Ubuntu下安装libz库：`sudo apt-get install zlib1g-dev`，然后使用`-lz`去连接。
- Ubuntu下安装BSD库：`sudo apt-get install libbsd-dev`，然后使用`-lbsd`去连接。此外，在`<bsd/stdlib.h>`中可使用 **arc4random** 等函数。
- Ubuntu下安装glib库：`sudo apt-get install libglib2.0-dev`。主要头文件为：`<glib.h>`。使用`pkg-config --cflags glib-2.0`可观察详细编译选项；使用`pkg-config --libs glib-2.0`可详细查看需要连接的库。如果我们要使用gobject库，那么将上述查看编译和连接选项的库名改为`gobject-2.0`即可。gobject库的头文件为：`<glib-object.h>`。
- [GLib开源项目](https://gitlab.gnome.org/GNOME/glib)
- Ubuntu下查看当前所有可安装的软件包：`dpkg -l`。
- [Download C# Mono](https://www.mono-project.com/download/stable/#download-lin)（安装完整的Mono：`sudo apt-get install mono-complete`。安装Monodevelop IDE：`sudo apt-get install monodevelop`。不过在树莓派上无法安装Monodevelop IDE，因此直接编译C#代码使用`mcs`命令，可直接生成可执行代码。对于mcs命令，使用`-unsafe`选项可启用非安全代码。）
- [.net、mono和C#](https://www.cnblogs.com/kekec/p/7237156.html)
- [.NET Core3.0开发Liunx桌面应用程序主要是依靠GTK](https://www.cnblogs.com/kgxk/p/11875769.html)
- [Nsight Eclipse Plugins Edition Getting Started Guide](https://docs.nvidia.com/cuda/nsight-eclipse-plugins-guide/index.html)
- [人工智能开发必须掌握的那些Linux指令（高级篇）](https://mp.weixin.qq.com/s/k3XuvGMV71gmDhhhLmL23w)

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

## Ubuntu下安装CUDA以及其自带驱动

以下文档文档可供参考：
- [Ubuntu 卸载 Nvidia 驱动和安装最新驱动](https://blog.csdn.net/wm9028/article/details/110268030)
- [在linux上安装cuda的时候报错：Existing package manager installation of the driver found.](https://blog.csdn.net/weixin_41010198/article/details/109367449)

1. 先在Ubuntu上卸载原始自带的nVidia驱动，它通常为Linux开源驱动：
```bash
sudo apt-get remove --purge nvidia*
sudo apt autoremove
sudo apt-get --purge remove "*nvidia*"

# 查看系统中安装了哪些nVidia驱动，如果全都删除的话应该不会有任何库出现
sudo dpkg --list | grep nvidia-*
```
2. 由于安装NV显卡驱动过程中不能使用X Window界面，因此我们必须进入命令行，关闭图形窗口界面。
首先按下`Ctrl + Alt + F1`进入命令行模式，然后分别输入用户名和密码。
3. 然后关闭X Server服务：`sudo stop lightdm`
4. `sudo init 3`
5. 重新输入用户名和密码。
6. 运行CUDA安装run文件：`sudo bash NVIDIA-Linux-x86_64-xxx.yy.zz.run`
7. 最后重启：`sudo reboot`

<br />

## CentOS下安装CUDA驱动

1. 准备环境设置：
```bash
chmod -R 777 /home/;chmod -R 777 /opt/;yum -y install gcc kernel-devel kernel-headers;mv /boot/initramfs-$(uname -r).img /boot/initramfs-$(uname -r).img.bak;dracut /boot/initramfs-$(uname -r).img $(uname -r);echo blacklist nouveau >>/usr/lib/modprobe.d/dist-blacklist.conf;echo options nouveau modeset=0 >>/usr/lib/modprobe.d/dist-blacklist.conf
```
2. 退出GUI桌面：
```bash
systemctl stop gdm.service
```
3. 运行安装文件（run文件）：
```bash
bash /mnt/andy/soft-all-for-linux/2xianka-install/NVIDIA-Linux-x86_64-390.48.run 
```
4. 卸载驱动：
```bash
bash /mnt/andy/soft-all-for-linux/2xianka-install/NVIDIA-Linux-x86_64-390.48.run  --uninstall
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

## C\# mono的使用

先创建一个csharp文件名，比如：**`CSTest.cs`**。然后输入以下代码：

```cs
using System;

class CSTest
{
    static void Main(string[] args)
    {
        Console.WriteLine("Hello, C#");
    }
}
```

最后在命令行进入到该源文件所在目录，然后输入：`mcs CSTest.cs`，最后就会生成CSTest.exe可执行文件。

<br />

## 安装LLVM-Clang

```shell
sudo apt-get install llvm

sudo apt-get install clang

sudo apt-get install libdispatch-dev
```
从GCC 8起，Clang 6起可以使用`-std=gnu17`标准。

<br />

## vim常用命令

- ESC: 进入命令状态
- a: 从命令状态进入编辑状态

命令状态下：
- `:q` 退出，不保存
- `:wq` 退出，且保存
- 强制退出并保存：`:wq!`

<br />

## FreeBSD相关

- [NETGRAPH](https://www.freebsd.org/cgi/man.cgi?query=netgraph&sektion=4)
- [netmap(4)](https://www.unix.com/man-page/freebsd/4/netmap/)
- [sctp(4)](https://www.unix.com/man-page/freebsd/4/sctp/)


