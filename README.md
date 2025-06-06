# Linux-based Development
Linux（主要基于Debian系）系统下的开发资料

<br />

## Contents

- [Resource List](#resource_list)
- [GCC内联汇编相关技巧（Clang编译器亦与之兼容）](#gcc_inline_assembly)
- [GCC使用 **`naked`** 与 **`-fomit-frame-pointer`** 优化属性来生成不依赖编译器的纯内联汇编函数](#gcc_naked_fomit-frame-pointer)
- [Linux 系统下获取当前机器的IPv4地址](#fetch_ipv4_address)
- [Linux 系统下获取当前机器的 Multicast IPv4 地址](#fetch_multicast_ipv4_address)
- [Raspbian系统下所需要安装的开发工具](#raspbian_utilities)
- [Ubuntu下安装CUDA以及其自带驱动](#ubuntu_cuda)
- [CentOS下安装CUDA驱动](#centos_cuda)
- [GNUstep编译选项](#gnustep_compile)
- [GTK+下载安装及编程指南资料汇总](#gtkplus_resource)
- [C\# mono的使用](#csharp_mono)
- [安装LLVM-Clang](#install_llvm-clang)
- [vim常用命令](#vim_commands)
- [FreeBSD相关](#freebsd_resource)

<br />

<a name="resource_list" id="resource_list"></a>
## Resource List

- [ChinaLinuxKernel-CLK](https://github.com/ChinaLinuxKernel/CLK)
- [GitLab CI Pipeline Stage Timeout](https://stackoverflow.com/questions/38403681/gitlab-ci-pipeline-stage-timeout)
- [GitLab CI/CD Set job start timeout](https://forum.gitlab.com/t/set-job-start-timeout/34993)
- [LinuxVersions](https://kernelnewbies.org/LinuxVersions)
- Linux显示当前目录的 **绝对路径** 命令：**`pwd`**。
- [Linux 下载文件命令](https://blog.csdn.net/hitabc141592/article/details/7561239)
- [Linux curl命令详解](https://www.cnblogs.com/duhuo/p/5695256.html)
- [Linux下的tar压缩解压缩命令详解](https://www.cnblogs.com/qq78292959/archive/2011/07/06/2099427.html)
- Linux下使用 zip 来压缩文件夹：`zip -r dst_file.zip src_folder_path`。
- Linux下使用 unzip 来解压文件：`unzip src_file.zip -d dst_folder_path`。
- [Linux下的mv命令](https://www.cnblogs.com/peida/archive/2012/10/27/2743022.html)
- Linux 下查看当前目录每个顶层子目录的空间占用大小：`du -h --max-depth=1 ./`
- [vi 常用命令行](https://www.cnblogs.com/sunormoon/archive/2012/02/10/2345326.html)（文件保存退出一般使用`:x`命令）
- [Linux文件查找命令](https://blog.csdn.net/qq_27517377/article/details/78870293)
- [Linux系统下查看文件与磁盘空间大小](https://www.cnblogs.com/adolfmc/archive/2013/02/16/2913801.html)
- [Linux的秘密：这才是find的正确使用姿势](https://www.toutiao.com/i6549496730935624195/)
- [从今往后，谁再告诉你Linux上chmod -R 777解决权限，果断绝交](https://www.toutiao.com/a6811852198561972744/)
- [Linux创建快捷方式的几种方法](https://blog.csdn.net/qq_41115033/article/details/123829766)（通常使用这种方式：**`sudo ln -s /opt/lib/libapp.so.6  /usr/lib/libapp.so`**）
- [linux拷贝软连接文件](https://www.cnblogs.com/macrored/p/11753862.html)（拷贝含有软链接文件的文件夹，可以使用 **`-frL`**，使得里面所有的软链接文件变成独立的它原本所链接到的目标文件的拷贝。通常用这种方式可以将包含软链接文件的文件夹拷贝到网盘、U盘等其他存储介质。）
- [在Linux=＞(Centos,Ubuntu)系统中如何查找最大的10个文件方法汇总](https://blog.csdn.net/qq_34246965/article/details/110038468)
- Linux下SSH命令远程连接服务器：`ssh username@server_ip_address`。比如：`ssh admin@192.168.1.100`。退出登录使用 **`exit`** 命令。
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
- [Linux革命性工具，shell脚本自动化](https://www.toutiao.com/article/7187343867296203324/)
- [Linux Shell 参数](https://wenku.baidu.com/view/ea25bd14e75c3b3567ec102de2bd960590c6d9f9.html)
- [Linux Shell脚本中获取本机ip地址方法](https://www.cnblogs.com/lidabo/p/15926304.html)
- [linux常见系统环境变量](https://www.cnblogs.com/renping/p/7020354.html)
- [linux c 编程 环境变量的操作函数](https://blog.csdn.net/q435201823/article/details/107163816)
- Linux 上将控制台执行命令的输出重定向转存到某一文件：`<command> | tee /tmp/log.txt`。如果想把 **`stderr`** 重定向到 **`stdout`**：`<command> 2>&1 | tee /tmp/log.txt`；如果此条命令产生歧义重定向，则尝试使用：`<command> >& /tmp/file.log`。
- [Linux连不上网解决](https://www.cnblogs.com/lbky/articles/11023246.html)
- Unix/Linux下如何查看DNS服务器地址：可使用命令 **`cat /etc/resolv.conf`** 或是 **`less /etc/resolv.conf`**。详细可参考：[How To Find Out What My DNS Servers Address Is](https://www.cyberciti.biz/faq/how-to-find-out-what-my-dns-servers-address-is/)
- [Linux下实时查看GPU状态](https://blog.csdn.net/zhang_yang_43/article/details/78357458)
- [A Step-By-Step Guide To Install CMake On Linux](https://www.linuxfordevices.com/tutorials/install-cmake-on-linux)（Linux系统安装 **CMake** 的关键命令：**`sudo sh cmake.sh --prefix=/usr/local/ --exclude-subdir`**。The above command will install cmake globally for all users to **`/usr/local/bin`** and the **`--exclude-subdir`** option is to get rid of the extra directory that is produced while extracting the .tar.gz archive.）
- [Linux（centos）下卸载及安装cmake详细步骤](https://blog.csdn.net/qq_22159287/article/details/121916753)
- [linux下卸载旧版本cmake安装新版本cmake](https://blog.csdn.net/qq_40164094/article/details/120196560)
- [linux环境下基于VSCode配置多目录C/C++编译调试环境](https://blog.csdn.net/qq_51482778/article/details/137018621)
- [Linux环境使用VSCode调试简单C++代码](https://zhuanlan.zhihu.com/p/618040277)
- [Ubuntu下VScode代码字体设置——monospace（等宽字体）](https://blog.csdn.net/xuw_xy/article/details/116101147)
- [Sound recording program using Nano](https://raspberrypi.stackexchange.com/questions/15018/sound-recording-program-using-nano)
- [Install alsa-utils on Ubuntu: sudo apt-get install alsa-utils](https://www.devmanuals.net/install/ubuntu/ubuntu-12-04-lts-precise-pangolin/install-alsa-utils.html)
- [Sound Recording & Play on Raspberry Pi Using ALSA in C](https://stackoverflow.com/questions/38615396/sound-recording-play-on-raspberry-pi-using-alsa-in-c)
- [使用ALSA检查声卡驱动](https://www.alsa-project.org/wiki/SoundcardTesting)（在Linux下，**alsamixer** 工具在 `/usr/bin/alsamixer`下，使用F6可切换声卡。也可以使用 `arecord -l` 命令来列出支持麦克风声卡的驱动。）
- [【Linux&音频】Alsa音频编程【精华】](https://www.cnblogs.com/lifan3a/articles/5481993.html)
- [ALSA（高级Linux声音架构）浅析](https://mp.weixin.qq.com/s?__biz=MzUxMjEyNDgyNw==&mid=2247512379&idx=1&sn=8d9d4c609bfc1901a4613f39b198ee5a)
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
- [linux Bluetooth programming in c](https://stackoverflow.com/questions/11408609/linux-bluetooth-programming-in-c)
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
- [Events: Input from a Window](http://www-h.eng.cam.ac.uk/help/tpl/graphics/X/X11R5/node25.html)（基于 X-Window 的 XLib）
- Ubuntu 安装 X-Window 的 Xlib 库：`sudo apt install libx11-dev`
- [Ubuntu安装opengl es2.0和egl库](https://blog.csdn.net/qq_41006901/article/details/103260569)（先检查一下当前私有驱动是否已经包含了EGL库。比如见以下链接）
- [Unable to use EGL without X Server on Ubuntu](https://stackoverflow.com/questions/49849033/unable-to-use-egl-without-x-server-on-ubuntu)
- Raspbian安装OpenGL ES与EGL：`sudo apt-get install libva-egl1 libegl1-mesa-drivers gegl libgles2-mesa-dev libglfw-dev`
- [Only OpenGL ES 1.1 and not 2.0 on Raspberry Pi 3](https://stackoverflow.com/questions/48136077/only-opengl-es-1-1-and-not-2-0-on-raspberry-pi-3)
- [Dispmanx -- Raspberry Pi Dispmanx windowing system](https://github.com/AndrewFromMelbourne/raspidmx)
- [Raspberry Pi VideoCore APIs](https://elinux.org/Raspberry_Pi_VideoCore_APIs)
- [linux下获取按键响应事件](https://www.cnblogs.com/yangwindsor/articles/3454955.html)（这种方式是阻塞式的）
- [Raspbian下在EGL环境中捕获键盘按键响应事件](https://github.com/AndrewFromMelbourne/raspidmx/blob/master/common/key.c)（Linux下获得鼠标事件可参考Raspbian系统下`/opt/vc/src/hello_pi/hello_triangle2`这一demo。）
- [Welcome to the Raspberry Pi Documentation](https://github.com/raspberrypi/documentation)
- [Linux BSP实战课（clock 驱动篇）：时钟子系统的实现](https://www.toutiao.com/article/7306328442440892964/)
- [Linux下的进程间通信：共享存储](https://www.toutiao.com/a6688140435799409160)
- [共享内存才是实现进程间通信最简单也是最直接的方法](https://www.toutiao.com/a6736813277818389006/)
- [Linux共享内存使用常见陷阱与分析](https://zhuanlan.zhihu.com/p/260418383)
- [Linux内核中的软中断、tasklet和工作队列](http://blog.csdn.net/T146lLa128XX0x/article/details/79070798)
- [zpoline: system call hook for Linux](https://github.com/yasukata/zpoline/tree/master)
- [Linus Torvalds掷下重锤：Linux 6.11中的可扩展调度程序sched_ext](https://www.toutiao.com/article/7379416523910808075/)（**DSQ**: dispatch queues）
- [多线程 or 多进程？](https://blog.csdn.net/zy799894671/article/details/18405033)
- [Getting Started with Intel® Threading Building Blocks \(Intel® TBB\)](https://www.intel.com/content/www/us/en/developer/articles/guide/get-started-with-tbb.html)
- [Linux内核如何替换内核函数并调用原始函数](https://blog.csdn.net/dog250/article/details/84201114)
- [Netflix 团队解决了 Linux 内核中的 FUSE 死锁](https://www.toutiao.com/article/7235624836679205410/)
- [怎样Hack Linux的内核符号？](https://blog.csdn.net/sinat_30551659/article/details/107705842)
- [How To Install LLVM and Clang on CentOS 6](https://www.vultr.com/docs/how-to-install-llvm-and-clang-on-centos-6)
- [在Centos-5下安装Objective-C的编译环境](http://blog.csdn.net/Robincui2011/article/details/6785987)
- [浅谈 Linux下的零拷贝机制](https://www.toutiao.com/i6462135845481611790/)
- [零拷贝(zero copy)技术你真的懂吗？什么时候需要用到内存映射？](https://www.modb.pro/db/23696)
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
- [DMA，Direct IO和零拷贝](https://www.toutiao.com/i6945819523622666782/)
- [浅谈mmap介绍](https://www.toutiao.com/a6756789193474572808/)
- [linux库函数mmap\(\)原理及用法详解](https://blog.csdn.net/qq_41687938/article/details/119901916)
- [3 万字 + 40 张图 ｜ 拆解 mmap 内存映射的本质！](https://www.toutiao.com/article/7340927008223822348/)
- [在Linux中利用mmap模拟Windows的 **`VirtualAlloc`**](https://blog.csdn.net/cjfeii/article/details/9122279)
- [Is it possible to allocate large amount of virtual memory in linux?](https://stackoverflow.com/questions/58523977/is-it-possible-to-allocate-large-amount-of-virtual-memory-in-linux)
- [深入理解 Linux 内核--jemalloc 引起的 TLB shootdown 及优化](https://www.toutiao.com/a6801053138380915211/)
- [Memory Allocation Guide](https://www.kernel.org/doc/html/latest/core-api/memory-allocation.html)
- [Linux系统监控：虚拟内存](https://www.cnblogs.com/luoahong/articles/7911266.html)
- [linux虚拟内存，内存及内存管理相关](https://blog.csdn.net/chen_jianjian/article/details/88876392)
- [万字长文，别再说你不懂Linux内存管理了（合辑），30 张图给你安排的明明白白](https://mp.weixin.qq.com/s?__biz=MzI3ODQ3OTczMw==&mid=2247493251&idx=1&sn=10d495947c4849c6cf854b15e7f6e7c5&chksm=eb54f099dc23798fce0f5db05e080bb0830133504dcfed325c66c2dcae6f4176b36484225676&mpshare=1&scene=23&srcid=01094DqUSLSGFRKOOLtfpqsU)
- [深入理解glibc malloc：malloc() 与 free() 原理图解](https://www.toutiao.com/i7046286983177470500/)
- [使用 malloc_trim\(\)](https://blog.csdn.net/CaspianSea/article/details/72457221)
- [malloc_trim\(3\) — Linux manual page](https://man7.org/linux/man-pages/man3/malloc_trim.3.html)
- [malloc_usable_size\(3\) — Linux manual page](https://man7.org/linux/man-pages/man3/malloc_usable_size.3.html)
- [Linux内核Page Cache和Buffer Cache关系及演化历史](https://www.toutiao.com/a6816861382776979976/)
- [Linux内核快速处理路径尽量多用slab而慎用kmalloc](https://blog.csdn.net/dog250/article/details/105544111)
- [Linux内存管理：NUMA技术详解（非一致内存访问架构）](https://blog.csdn.net/Rong_Toa/article/details/109137312)
- [Is there a canonical programmatic way to query for the set of cores belonging to a NUMA node?](https://stackoverflow.com/questions/51031674/is-there-a-canonical-programmatic-way-to-query-for-the-set-of-cores-belonging-to)
- [CPU_SET(3) — Linux manual page](https://www.man7.org/linux/man-pages/man3/CPU_SET.3.html)
- 获得当前的 **CPU ID** 可以使用：[sched_getcpu](https://www.man7.org/linux/man-pages/man3/sched_getcpu.3.html)
- [libnuma详解(A NUMA API for LINUX)](https://blog.csdn.net/qq_40379678/article/details/107814666)
- [libnuma 及底层实现](https://blog.csdn.net/phone1126/article/details/134194067)
- [numactl](https://github.com/numactl/numactl)：**libnuma**
- Ubuntu 安装 **libnuma**：**`sudo apt-get install libnuma-dev`**
- [numa(3) — Linux manual page](https://www.man7.org/linux/man-pages/man3/numa.3.html)
- [聊聊文件IO](https://www.toutiao.com/a6700806648274878987)
- [存储进阶：怎么才能保证 IO 数据的安全？](https://www.toutiao.com/i6959376691781190151/)
- [分钟搞懂Linux中直接I/O原理](https://www.toutiao.com/a6701654059910169091/)
- [高级程序员进阶：了解Linux I/O 调度器，优化系统性能](https://www.toutiao.com/a6735373272432509452/)
- [C语言IPC函数指南汇总整理](https://www.toutiao.com/article/7397021219326902824/)
- [Linux网络编程-socket编程](https://blog.csdn.net/weixin_73625390/article/details/130956912)
- Linux 为 socket 设置读写超时：

```c
        int connectSock = socket(AF_INET, SOCK_STREAM, 0);
        if (connectSock < 0)
        {
            fprintf(stderr, "socket failed with error: %d\n", errno);
            return;
        }
        // setting for 7 seconds timeout
        const struct timeval timeout { .tv_sec = 7, .tv_usec = 0 };

        // Set receive timeout
        int result = setsockopt(connectSock, SOL_SOCKET, SO_RCVTIMEO, &timeout, (socklen_t)sizeof(timeout));
        if (result < 0)
        {
            fprintf(stderr, "setsockopt for receive timeout failed with error: %d\n", errno);
            break;
        }

        // Set send timeout
        result = setsockopt(connectSock, SOL_SOCKET, SO_SNDTIMEO, &timeout, (socklen_t)sizeof(timeout));
        if (result < 0)
        {
            fprintf(stderr, "setsockopt for send timeout failed with error: %d\n", errno);
            break;
        }
```

- Linux 使用 **`getaddrinfo`** 获取IP地址：

```c
#include <stdio.h>
#include <errno.h>

#include <unistd.h>
#include <sys/types.h>
#include <sys/time.h>
#include <sys/socket.h>
#include <fcntl.h>
#include <arpa/inet.h>
#include <netdb.h>

static const char* const IP_ADDRESS = "127.0.0.1";
static const char* const PORT_NUMBER = "5678";

static void ClientTest(void)
{
    struct addrinfo hints { .ai_family = AF_INET, .ai_socktype = SOCK_STREAM, .ai_protocol = IPPROTO_TCP };
    struct addrinfo *resAddrInfo = NULL;
    int result = getaddrinfo(IP_ADDRESS, PORT_NUMBER, &hints, &resAddrInfo);
    if(result != 0)
    {
        fprintf(stderr, "getaddrinfo failed with error: %s\n", gai_strerror(result));
        return;
    }

    // TODO: Insert client socket connection code here...
    int connectSock = socket(AF_INET, SOCK_STREAM, 0);
    if (connectSock < 0)
    {
        fprintf(stderr, "socket failed with error: %d\n", errno);
        return;
    }

    result = connect(connectSock, resAddrInfo->ai_addr, resAddrInfo->ai_addrlen);
    if (result < 0)
    {
        fprintf(stderr, "connect failed with error: %d\n", errno);
        if(errno == EINPROGRESS) {
            fprintf(stderr, "The connection request has been initialized but is still in progress!\n");
        }
        return;
    }

    // Release the IP address info object
    if(resAddrInfo != NULL) {
        freeaddrinfo(resAddrInfo);
    }
}
```

- Linux系统下获取当前机器 IPv4 地址的 shell 命令：

```shell
ip addr show | grep 'inet ' | awk '{print $2}' | cut -d/ -f1 | grep -v "127.0.0.1"
```

- Linux系统下获取当前机器 Multicast IPv4 地址的 shell 命令：

```shell
ip maddr show | grep 'inet ' | awk '{print $2}' | cut -d/ -f1 | grep -v "224.0.0.1"
```

- [linux 网络协议.之UDP Socket通信，单播，组播，广播（四）](https://blog.csdn.net/rjszcb/article/details/121557382)
- [epoll原理简介](https://www.toutiao.com/a6701457609444033031)
- [如果这篇文章说不清epoll的本质，那就过来掐死我吧！](https://www.toutiao.com/a6683264188661367309)
- [高并发高吞吐IO秘密武器——epoll池化技术](https://www.toutiao.com/i7008441343617794563/)
- [6种epoll的设计，让你吊打面试官，而且他不能还嘴](https://www.toutiao.com/i7009187407606088223/)
- [epoll 在 IO 密集时为什么效率不高](https://www.toutiao.com/video/7382411285457011240/)
- [非阻塞 I/O 和多路复用+select、poll、epoll模型详解](https://www.toutiao.com/i6554223409138500110)
- [腾讯面试：请描述 select、poll、epoll 这三种技术的执行原理](https://www.toutiao.com/article/7427350508605669897/)
- [sendfile 和 epoll](https://blog.csdn.net/amaowolf/article/details/7418792)
- [io_submit：Linux内核新加入的epoll替代方案](https://www.toutiao.com/a6809889593286984206/)
- [AIO 的新归宿：io_uring](https://zhuanlan.zhihu.com/p/62682475)
- [io_uring只适用于存储IO？大错特错](https://www.toutiao.com/i6884987457641644551/)
- [io_uring vs epoll，谁在网络编程领域更胜一筹？](https://www.toutiao.com/i7045101452641124877/)
- [Linux下全新的异步I/O：io_uring详解](https://www.toutiao.com/i7011043732220805668/)
- [linux异步IO编程实例分析](https://www.toutiao.com/a6875582313590325774/)
- [kqueue用法简介](https://www.cnblogs.com/luminocean/p/5631336.html)
- [使用kqueue在FreeBSD上开发高性能应用服务器](http://www.ibm.com/developerworks/cn/aix/library/1105_huangrg_kqueue/)
- [Linux AIO 异步读写](https://www.cnblogs.com/standardzero/p/12552642.html)
- [异步唤醒机制：**`eventfd`** 和条件变量区别](https://www.toutiao.com/article/7258483579754234408/)
- [最专业的对“鸿蒙”的分析](https://www.toutiao.com/a7039879650885222951/)
- [使程序在Linux下后台运行 （关掉终端继续让程序运行的方法）](https://www.cnblogs.com/little-ant/p/3952424.html)
- GAS下使用Intel语法汇编并且在寄存器前不添加 `%` 符号：`.intel_syntax noprefix`。
- GCC/Clang编译器下要使用 `<intrin.h>`，则得：`#include <x86intrin.h>`。
- [How do I call “cpuid” in Linux?](https://stackoverflow.com/questions/14266772/how-do-i-call-cpuid-in-linux)
```c
#include <cpuid.h>

// Return highest supported input value for cpuid instruction.
// @param ext can be either 0x0 or 0x8000000 to return highest supported value for basic or extended cpuid information.
// Function returns 0 if cpuid is not supported or whatever cpuid returns in eax register.
// @sig If sig pointer is non-null, then first four bytes of the signature (as found in ebx register) are returned in location pointed by sig.
unsigned int __get_cpuid_max (unsigned int __ext, unsigned int *__sig);

// Return cpuid data for requested cpuid level, as found in returned eax, ebx, ecx and edx registers.
// The function checks if cpuid is supported and returns 1 for valid cpuid information, or 0 for unsupported cpuid level.
// All pointers are required to be non-null.
int __get_cpuid (unsigned int __level,
    unsigned int *__eax, unsigned int *__ebx,
    unsigned int *__ecx, unsigned int *__edx);
```
- [Converting a C source code to LLVM assembly](https://www.oreilly.com/library/view/llvm-cookbook/9781785285981/ch01s04.html)
- [gcc在代码中禁止某些warning](https://www.cnblogs.com/jhj117/p/6639111.html)
- [gcc, g++编译时消除特定警告的方法](https://blog.csdn.net/li_wen01/article/details/71171413)
- [Suppressing Warnings in GCC and Clang](https://nelkinda.com/blog/suppress-warnings-in-gcc-and-clang/)
- [gcc 编译 gcc warning 'variable tracking size limit exceeded' 原因及解决办法](https://blog.csdn.net/photon222/article/details/89217737)
- [严格别名规则“-fstrict-aliasing”和“-fno-strict-aliasing”及类型双关](https://www.cnblogs.com/aquester/p/10299471.html)
- GCC对某一函数启用`-O2`编译选项并禁用`strict-aliasing`：`__attribute__((optimize("-O2"), optimize("-fno-strict-aliasing")))`
- [Clang对指定函数禁用优化](https://clang.llvm.org/docs/AttributeReference.html#optnone) —— 比如：
```cpp
[[ clang::optnone ]] void foo(void) {  }
```
- GCC编译器指定结构体对齐：`-fpack-struct=n`。
- GCC与Clang使用打包的结构体：
```cpp
#if __clang__
    struct [[gnu::packed]]
#else
    struct __attribute__((packed))
#endif
    SS { long long a; int b; long long c; };

    static_assert(sizeof(SS) == 20);
```
- GCC上对于用 **`-D`** 定义的预处理符号，如果其值包含双引号 **`"`**，则需要使用转义符 **` \ `**。比如：`-DMY_NAME=\"Smith\"`。
- [GCC编译宏_GLIBCXX_USE_CXX11_ABI背景分析和实现原理](https://blog.csdn.net/ithiker/article/details/126447778)
- GCC默认连接静态库使用此连接选项：`-static`。
- [Linux 使用静态库注意事项](https://www.bbsmax.com/A/obzbmvVbdE/)
- [如何编译静态库及将多个.a静态库合并成一个.a静态库](https://www.pianshen.com/article/77691341/)
- Linux下生成动态库使用 **`-fPIC`** 编译选项以及 **`-shared`** 连接选项，并且动态库的命名规则为：lib<lib-name>.so。加载动态库时使用`export LD_LIBRARY_PATH=`导出动态库所在路径。
- [动态库链接静态库防止符号污染（使用 **`-Wl,--exclude-libs,ALL`** 连接器选项）](https://blog.csdn.net/u014789533/article/details/128613071)
- 用GCC编译C++代码时最好使用 `g++`，否则会导致一些特定的C++函数符号找不到。如果遇到某些引用STL库的函数而引发符号找不到错误，则可尝试添加 `-lstdc++` 来解决。
- GCC上对于静态库或动态库文件名不以`lib`作为前缀的情况下可在连接时直接用该文件名去连。比如我们要连接一个`libtest.so`和`testlib.so`，我们可以用：`gcc -ltest testlib.so -o target`。
- [Anatomy of Linux dynamic libraries](https://developer.ibm.com/tutorials/l-dynamic-libraries/) （The option **`-rdynamic`** is used to tell the linker to add all symbols to the dynamic symbol table (to permit backtraces with the use of dlopen). The **`-ldl`** indicates that the dllib should be linked to this program.）
- [GCC的符号可见性 -fvisibility=hidden](https://blog.csdn.net/qq_38350702/article/details/106128157)（它属于编译选项）
- [使用GCC导出C++类的符号(Export symbols of C++ class with GCC)](https://www.656463.com/wenda/shiyongGCCdaochuCleidefuhao_493)（要生成可被运行时动态加载的动态库时，可使用 **`-shared -s -Wl,--export-dynamic`** 这些连接器选项）
- [What are the meanings of the columns of the symbol table displayed by **readelf**?](https://stackoverflow.com/questions/3065535/what-are-the-meanings-of-the-columns-of-the-symbol-table-displayed-by-readelf)（具体使用时最好再加上 **`-W`** 选项，以免某些符号过长而被自动截断。比如：**`readelf -W -s libdll.so`**）
- GCC使用 **`-s`** 连接器选项将所有符号表及重定向信息从可执行文件或动态连接库中移除。
- [version 'GLIBC_2.34' not found简单有效解决方法](https://blog.csdn.net/huazhang_001/article/details/128828999)
- 用 cmake 将 yaml 静态库打包到libcis.so 这个动态库后，加载这个libcis.so 这个动态库 出现 `undefined symbol: _ZTIN4YAML13BadConversionE` 这个问题怎么解决：这通常是因为链接顺序不正确导致的。确保在CMakeLists.txt中正确设置了链接顺序。确保在生成libcis.so动态库时，将yaml静态库放在链接命令的末尾。
- [linux中的ld命令及其搜索路径顺序](https://blog.csdn.net/qq_42731705/article/details/123934842)
- [干货！gcc和g++编译器有什么区别？看完这篇就明白了](https://www.toutiao.com/article/7194762934655091252/)
- [记录linux 生成crash dump文件步骤](https://blog.csdn.net/dengdun6257/article/details/102283543)
- [How can I read a crash file from `/var/crash`](https://askubuntu.com/questions/434431/how-can-i-read-a-crash-file-from-var-crash)（对于比较大的 CoreDump 文件，本回答的第3条操作可能失败，可直接参考上面那篇文章对 CoreDump 的打开方式，最后再用本回答的第4条。）
- [gcc命令objdump用法----反汇编](https://blog.csdn.net/cwcwj3069/article/details/8273129)
- [Linux环境定位C程序内存泄露以及非法访问的方法](https://blog.csdn.net/xingyeping/article/details/72828788)
- [Bytehound - a memory profiler for Linux](https://github.com/koute/bytehound)
- [linux 强制32位编译,使用CMake强制进行32位编译的正确方法](https://blog.csdn.net/weixin_34952628/article/details/116756981)
- [Linux下C语言如何使用定时器功能](https://www.cnblogs.com/chorm590/p/12158395.html)
- [linux下常用的几个时间函数：gettimeofday和clock_gettime](https://blog.csdn.net/fchyang/article/details/81166470)（使用精确时间戳，直接使用`clock_gettime(CLOCK_MONOTONIC, &timespec);`。）
**`gettimeofday`** 使用例子如下：
```c
#include <sys/time.h>

int main(void)
{
    struct timeval tBegin, tEnd;
    gettimeofday(&tBegin, NULL);

    int count = 0;
        
    for(int i = 0; i < 1000 * 1000; i++) {
        count += i;
    }
        
    gettimeofday(&tEnd, NULL);
        
    long deltaTime = 1000000L * (tEnd.tv_sec - tBegin.tv_sec ) + (tEnd.tv_usec - tBegin.tv_usec);

    printf("Time spent: %ldus\n", deltaTime);
}
```

![gcc_option_order](images/gcc_option_order.jpg)

- [Linux下C语言获取目录中的文件列表](https://www.cnblogs.com/dgwblog/p/12158373.html)
- [操作系统的中打开文件的最大句柄数](https://blog.csdn.net/qq_26685237/article/details/106771340)
- [Linux下的sleep()和usleep()的使用和区别](https://www.cnblogs.com/ZhaoxiCheung/p/6792734.html)
- **pthread** 获得当前线程句柄：[**pthread_self**](https://www.man7.org/linux/man-pages/man3/pthread_self.3.html)
- [pthread_cond_init](https://www.man7.org/linux/man-pages/man3/pthread_cond_init.3.html)
- [sched_yield\(2\) — Linux manual page](https://man7.org/linux/man-pages/man2/sched_yield.2.html)
- [gcc and `cpu_relax`, smb_mb, etc.?](https://stackoverflow.com/questions/47975191/gcc-and-cpu-relax-smb-mb-etc)
- [Spinlocks and Read-Write Locks](http://locklessinc.com/articles/locks/)
- [Linux 获取本机IP、MAC地址用法大全](https://www.cnblogs.com/fnlingnzb-learner/p/6427786.html)
- [C++ win32和linux获取系统剩余内存](https://blog.csdn.net/q1368232592/article/details/85157823)
- Linux获取当前系统分发版本信息：`cat /etc/os-release`
- [Linux下获取内核版本号的函数](https://blog.csdn.net/ly890700/article/details/53540653)
- [Linux系统调用--uname()函数及系统下的uname命令](http://blog.chinaunix.net/uid-8996150-id-2011653.html)
- Linux系统下使用 C API 获得当前逻辑处理器的总个数可使用：[**get_nprocs**](https://www.man7.org/linux/man-pages/man3/get_nprocs_conf.3.html)
- [Linux查看物理CPU个数、核数、逻辑CPU个数](https://www.cnblogs.com/bugutian/p/6138880.html)
- [Linux如何查看CPU信息，Linux查看CPU个数和核心数，Linux查看CPU使用率和运行位数](https://blog.csdn.net/tiiefu1212/article/details/78623132)
- [获取SYSTEM()执行结果](https://blog.csdn.net/u013625451/article/details/78830104)
- [类Unix系统中如何获取另一个程序的输出内容](https://baike.baidu.com/item/popen)
- [使用popen执行shell命令并获取返回结果](https://www.cnblogs.com/hiawind/p/9089288.html)
- [linux中open()函数的mode_t 含义](https://blog.csdn.net/sdhgood/article/details/39555311)（**`O_LARGEFILE`** 标志用于指示`off_t`无法容下文件大小而只能用`off64_t`）
- [教你写第一个Linux设备驱动程序](https://www.toutiao.com/a6812972562201444878/)
- [How do I set a software breakpoint on an ARM processor?](https://stackoverflow.com/questions/11345371/how-do-i-set-a-software-breakpoint-on-an-arm-processor)
- 对于不支持硬件断点的ARM Linux可使用 `raise(SIGTRAP)` 系统调用来触发gdb的断点调试。
- [通过篡改cred结构体实现提权利用](https://www.toutiao.com/article/7278957821289333283/)
- [Ubuntu系统下通过Clang编译器编写Objective-C](https://blog.csdn.net/zenny_chen/article/details/52507022)
- Ubuntu下安装libz库：`sudo apt-get install zlib1g-dev`，然后使用`-lz`去连接。
- Ubuntu下安装BSD库：`sudo apt-get install libbsd-dev`，然后使用`-lbsd`去连接。此外，在`<bsd/stdlib.h>`中可使用 **arc4random** 等函数。
- Ubuntu下安装glib库：`sudo apt-get install libglib2.0-dev`。主要头文件为：`<glib.h>`。使用`pkg-config --cflags glib-2.0`可观察详细编译选项；使用`pkg-config --libs glib-2.0`可详细查看需要连接的库。如果我们要使用gobject库，那么将上述查看编译和连接选项的库名改为`gobject-2.0`即可。gobject库的头文件为：`<glib-object.h>`。
- Ubuntu 安装 freetype：`sudo apt install libfreetype6-dev`。
- [Ubuntu安装VS Code](https://blog.csdn.net/weixin_44733606/article/details/131662272)
- [GLib开源项目](https://gitlab.gnome.org/GNOME/glib)
- Ubuntu下查看当前所有可安装的软件包：`dpkg -l`。
- [Download C# Mono](https://www.mono-project.com/download/stable/#download-lin)（安装完整的Mono：`sudo apt-get install mono-complete`。安装Monodevelop IDE：`sudo apt-get install monodevelop`。不过在树莓派上无法安装Monodevelop IDE，因此直接编译C#代码使用`mcs`命令，可直接生成可执行代码。对于mcs命令，使用`-unsafe`选项可启用非安全代码。）
- [.net、mono和C#](https://www.cnblogs.com/kekec/p/7237156.html)
- [.NET Core3.0开发Liunx桌面应用程序主要是依靠GTK](https://www.cnblogs.com/kgxk/p/11875769.html)
- Ubuntu 上卸载CUDA ToolKit：
```shell
cd /usr/local/cuda/bin/
sudo ./cuda-uninstaller
```
- [Nsight Eclipse Plugins Edition Getting Started Guide](https://docs.nvidia.com/cuda/nsight-eclipse-plugins-guide/index.html)（打开Eclipse，选择 Help，再选择 Install New Software… ，点击 Add 按钮，点击 Archive... 按钮，选择 `/usr/local/cuda/` 目录中的 `nsightee_plugins` 中的 zip 文件）
- [Using C++ on Linux in VS Code](https://code.visualstudio.com/docs/cpp/config-linux)
- [人工智能开发必须掌握的那些Linux指令（高级篇）](https://mp.weixin.qq.com/s/k3XuvGMV71gmDhhhLmL23w)

<br/>

<a name="gcc_inline_assembly" id="gcc_inline_assembly"></a>
## GCC内联汇编相关技巧（Clang编译器亦与之兼容）

- [gcc 内联汇编](https://blog.csdn.net/yanzhongqian/article/details/124482833)
- [ARM64基础11:GCC内嵌汇编补充](https://blog.csdn.net/luteresa/article/details/120140887)
- [如何在ARM aarch64中使用32位w寄存器进行GCC内联汇编？](https://cloud.tencent.com/developer/ask/sof/815815)

以下为几个常用例子：
```c
#include <stdbool.h>

// 常见的内联汇编方式
static inline int MyARM64Sub(int a, int b)
{
    int result;
    asm volatile ("sub    %w[dst], %w[src1], %w[src2]"
        : [dst] "=r" (result)
        : [src1] "r" (a), [src2] "r" (b));
    return result;
}

// 只有一个输出操作数
static inline unsigned MyGetFPCR(void)
{
    unsigned long long result;
    asm volatile ("mrs    %[result], fpcr" : [result] "=r" (result));
    return (unsigned)result;
}

// 只有一个输入操作数
static inline void MySetFPCR(unsigned fpcrValue)
{
    asm volatile ("msr    fpcr, %[fpcrValue]" : : [fpcrValue] "r" ((unsigned long long)fpcrValue));
}

// 参数expected在内联汇编中既作为输入操作数又作为输出操作数
static inline unsigned MyAtomicCAS_LSE(volatile void *dst, unsigned expected, unsigned newValue)
{
    asm volatile ("cas    %w[expected], %w[newValue], [%[dst]]"
        : [expected] "+r" (expected)
        : [newValue] "r" (newValue), [dst] "r" (dst));

    return expected;
}

static inline unsigned MyLDXR(const volatile void *ptr)
{
    unsigned result;
    asm volatile ("ldxr   %w[result], [%[ptr]]"
        : [result] "=r" (result)
        : [ptr] "r" (ptr));
    return result;
}

// 这里为了避免对不同变量使用相同的寄存器名，而特意指定相应的寄存器
static inline bool MySTXR(volatile void *dst, unsigned value)
{
    register volatile void *pDst asm("x2") = dst;
    register unsigned srcValue asm ("w1") = value;
    register bool result asm ("w0");

    asm volatile ("stxr   %w[result], %w[src], [%[dst]]"
        : [result] "=r" (result)
        : [src] "r" (srcValue), [dst] "r" (pDst));
    return result;
}

// 以上内联汇编的C函数在Android NDK平台下的测试：
const int result = MyARM64Sub(7, 3);
syslog(LOG_INFO, "The subtraction result: %d\n", result);

volatile unsigned data = 100;
unsigned expected = data;
expected = MyAtomicCAS_LSE(&data, expected, expected + 10);
syslog(LOG_INFO, "expected = %u\n", expected);
syslog(LOG_INFO, "now data = %u\n", data);

expected = MyLDXR(&data);
expected += 1000U;
const bool bRes = MySTXR(&data, expected);
syslog(LOG_INFO, "bRes = %d, expected = %u\n", bRes, expected);
syslog(LOG_INFO, "now data = %u\n", data);

MySetFPCR(0x07000000U);
expected = MyGetFPCR();
syslog(LOG_INFO, "Current FPCR: 0x%08X\n", expected);
```

<br />

<a name="gcc_naked_fomit-frame-pointer" id="gcc_naked_fomit-frame-pointer"></a>
## GCC使用 **`naked`** 与 **`-fomit-frame-pointer`** 优化属性来生成不依赖编译器的纯内联汇编函数

```c
#include <stdio.h>

static int s_var = 0;

static void __attribute__((naked, optimize("-fomit-frame-pointer")))
ExecInc(int *pValue,  const void *pExitAddr)
{
    asm(".intel_syntax noprefix \n"
        "inc dword ptr [rdi]  \n"
        "jmp rsi     \n"
        ".att_syntax");
}

static void __attribute__((naked, optimize("-fomit-frame-pointer")))
CallEntry(int *pValue, const void *pExitAddr, const void *pExecAddr)
{
    asm(".intel_syntax noprefix \n"
        "jmp rdx     \n"
        ".att_syntax");
}

static void __attribute__((naked, optimize("-fomit-frame-pointer")))
CallExit(void)
{
    asm(".intel_syntax noprefix \n"
        "ret    \n"
        ".att_syntax");
}

int main(int argc, const char* argv[])
{
    while(s_var < 10)
        CallEntry(&s_var, (void*)CallExit, (void*)ExecInc);

    printf("s_var = %d\n", s_var);
}
```

<br />

<a name="fetch_ipv4_address" id="fetch_ipv4_address"></a>
## Linux 系统下获取当前机器的 IPv4 地址

```c
#include <stdio.h>
#include <stdbool.h>

#include <unistd.h>
#include <sys/types.h>
#include <sys/time.h>
#include <sys/socket.h>
#include <fcntl.h>
#include <arpa/inet.h>
#include <netdb.h>
#include <poll.h>

static bool FetchCurrentIPv4Address(char dstIPAddr[16])
{
    char buffer[256] = { };
    int fds[2];
    pipe(fds);
    int backupFD = dup(STDOUT_FILENO);
    dup2(fds[1], STDOUT_FILENO);

    system("ip addr show | grep 'inet ' | awk '{print $2}' | cut -d/ -f1 | grep -v \"127.0.0.1\"");

    read(fds[0], buffer, sizeof(buffer));

    dup2(backupFD, STDOUT_FILENO);

    const size_t ipAddrLen = strlen(buffer);
    for(size_t i = 0; i < ipAddrLen; ++i)
    {
        if((buffer[i] < '0' || buffer[i] > '9') && buffer[i] != '.')
        {
            buffer[i] = '\0';
            break;
        }
    }

    strcpy(dstIPAddr, buffer);

    return true;
}
```

<br />

<a name="fetch_multicast_ipv4_address" id="fetch_multicast_ipv4_address"></a>
## Linux 系统下获取当前机器的 Multicast IPv4 地址

```c
#include <stdio.h>
#include <stdbool.h>

#include <unistd.h>
#include <sys/types.h>
#include <sys/time.h>
#include <sys/socket.h>
#include <fcntl.h>
#include <arpa/inet.h>
#include <netdb.h>
#include <poll.h>

static bool FetchCurrentMulticastIPv4Address(char dstIPAddr[16])
{
    char buffer[256] = { };
    int fds[2];
    pipe(fds);
    int backupFD = dup(STDOUT_FILENO);
    dup2(fds[1], STDOUT_FILENO);

    system("ip maddr show | grep 'inet ' | awk '{print $2}' | cut -d/ -f1 | grep -v \"224.0.0.1\"");

    read(fds[0], buffer, sizeof(buffer));

    dup2(backupFD, STDOUT_FILENO);

    const size_t ipAddrLen = strlen(buffer);
    for(size_t i = 0; i < ipAddrLen; ++i)
    {
        if((buffer[i] < '0' || buffer[i] > '9') && buffer[i] != '.')
        {
            buffer[i] = '\0';
            break;
        }
    }

    strcpy(dstIPAddr, buffer);

    return true;
}
```

<a name="raspbian_utilities" id="raspbian_utilities"></a>
## Raspbian系统下所需要安装的开发工具
```bash
sudo apt-get update

sudo apt-get install build-essential

# 如果在Ubuntu上安装GCC或使用`sudo apt-get install build-essential`失败，则需要先执行一下`sudo apt-get update`，更新之后再执行安装命令。

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

# 安装 autoconf
sudo apt install autoconf

# 安装 automake
sudo apt install automake

# 安装 M4
sudo apt install m4

# 安装 libtool
sudo apt install libtool

# 安装 makeinfo 相关工具
sudo apt install texinfo
```

<br />

<a name="ubuntu_cuda" id="ubuntu_cuda"></a>
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
首先按下`Ctrl + Alt + F1`进入命令行模式，或者是在控制台输入 `systemctl stop gdm` 命令来关闭图形服务，然后分别输入用户名和密码。
3. 然后关闭X Server服务：`sudo stop lightdm`
4. `sudo init 3`
5. 重新输入用户名和密码。
6. 运行CUDA安装run文件：`sudo bash NVIDIA-Linux-x86_64-xxx.yy.zz.run`
7. 最后重启：`sudo reboot`

如果安装过程中遇到内核编译失败，则很可能是因为当前所使用的 GCC 版本与构建当前系统内核的 GCC 版本不一致所导致的（通常而言，当前用的 GCC 版本老于内核构建所使用的 GCC 版本），那么需要将当前 GCC 版本更新到与内核构建时所使用的 GCC 版本一致才行。

详细可参考：[ubuntu22.04安装NVIDIA显卡驱动出错“Warning: Compiler version check failed”](https://blog.csdn.net/pkyang2004/article/details/148420144)

<br />

<a name="centos_cuda" id="centos_cuda"></a>
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

<a name="gnustep_compile" id="gnustep_compile"></a>
## GNUstep编译选项

我们通过执行以下命令来观察Objective-C编译时所需要的编译选项：`gnustep-config --objc-flags`    
执行以下命令查看Objective-C连接时所需要的加载选项：`gnustep-config --objc-libs`

整理之后：
```bash
export GCC_PATH=/usr/lib/gcc/arm-linux-gnueabihf/8/
gcc test.m -std=gnu11 -Os  -MMD -MP -DGNUSTEP -DGNUSTEP_BASE_LIBRARY=1 -DGNU_RUNTIME=1 -DGNUSTEP_BASE_LIBRARY=1 -fno-strict-aliasing -pthread -fPIC -Wall -DGSWARN -DGSDIAGNOSE -Wno-import -fgnu-runtime -fconstant-string-class=NSConstantString  -I. -I/usr/local/include/GNUstep -I/usr/include/GNUstep -I${GCC_PATH}include/  -rdynamic -L/root/GNUstep/Library/Libraries -L/usr/local/lib -L/usr/lib -lobjc -lm -lgnustep-base -o test
```

<br />

<a name="gtkplus_resource" id="gtkplus_resource"></a>
## GTK+下载安装及编程指南资料汇总

- GTK+官方指南：http://zetcode.com/tutorials/gtktutorial/
- GTK+官方指南的中文翻译：http://zetcode.com/tutorials/gtktutorial/chinese/
- GTK+的Wiki网址：http://en.wikipedia.org/wiki/GTK%2B
- GTK+的下载安装：http://zhidao.baidu.com/question/323664703.html ; http://blog.csdn.net/ouyangzhan/article/details/5734832
- GTK+中使用2D图形库时用的是GDK。这个是其官方地址：http://developer.gnome.org/gdk3/stable/
- 而GDK底层用的是Cairo库，要想了解这个这个库的话可以访问这个地址：http://cairographics.org/documentation/

#### 在Ubuntu下要下载安装GTK+执行以下步骤：

1. sudo apt-get install gnome-core-devel
1. sudo apt-get install libgtk*

如果 `gnome-core-devel` 命令由于Linux版本问题无法执行，可直接运行 `install libgtk*`，这个会将 `pkg-config` 在内的所有与 gtk 相关的库安装进去。
然后，我们可以在控制台输入：`pkg-config --cflags --libs gtk+-3.0` 来查看gtk+3.0所需要包含的所有头文件以及库的路径。

#### 基于Eclipse的IDE来开发GTK+3.0需要设置头文件路径和库的路径：

##### 头文件路径需要以下这些：

- `/usr/include/glib-2.0/`
- `/usr/include/atk-1.0/`
- `/usr/include/gdk-pixbuf-2.0/`
- `/usr/include/cairo/`
- `/usr/include/pango-1.0/`
- （64位）`/usr/lib/x86_64-linux-gnu/glib-2.0/include/`
- （32位）`/usr/lib/i386-linux-gnu/glib-2.0/include/`
- `/usr/include/gtk-3.0/`

##### 库路径需要包含：

-（64位）/usr/lib/x86_64-linux-gnu/
- （32位）`/usr/lib/i386-linux-gnu/`

##### 所需要的库有：

- `gtk-3`
- `gobject-2.0`
- `pangocairo-1.0`
- `gio-2.0`
- `atk-1.0`
- `gdk-3`
- `glib-2.0`

注意，Linux下的库文件名是前缀加lib然后再跟库名，再是 **.a** 或 **.so** 结尾。

#### GTK+ 3编译选项

查看当前环境的GTK+ 3编译选项：`pkg-config --cflags --libs gtk+-3.0`

整理之后：
```bash
export ABI_NAME=${HOSTTYPE}-${OSTYPE}
gcc main.c -std=gnu11 -I/usr/include/glib-2.0/ -I/usr/include/atk-1.0/ -I/usr/include/gdk-pixbuf-2.0/ -I/usr/include/cairo/ -I/usr/include/pango-1.0/ -I/usr/lib/${ABI_NAME}/glib-2.0/include/ -I/usr/include/gtk-3.0/ -L/usr/lib/${ABI_NAME}/ -lgtk-3 -lgobject-2.0 -lpangocairo-1.0 -lgio-2.0 -latk-1.0 -lgdk-3 -lglib-2.0    -o gtk-test
```

<br />

<a name="csharp_mono" id="csharp_mono"></a>
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

<a name="install_llvm-clang" id="install_llvm-clang"></a>
## 安装LLVM-Clang

```shell
sudo apt-get install llvm

sudo apt-get install clang

sudo apt-get install libdispatch-dev
```
从GCC 8起，Clang 6起可以使用`-std=gnu17`标准。

<br />

<a name="vim_commands" id="vim_commands"></a>
## vim常用命令

- ESC: 进入命令状态
- a: 从命令状态进入编辑状态

命令状态下：
- `:q` 退出，不保存
- `:wq` 退出，且保存
- 强制退出并保存：`:wq!`

<br />

<a name="freebsd_resource" id="freebsd_resource"></a>
## FreeBSD相关

- [NETGRAPH](https://www.freebsd.org/cgi/man.cgi?query=netgraph&sektion=4)
- [netmap(4)](https://www.unix.com/man-page/freebsd/4/netmap/)
- [sctp(4)](https://www.unix.com/man-page/freebsd/4/sctp/)


