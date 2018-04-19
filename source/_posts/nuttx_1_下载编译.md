---
title: nuttx第一步下载编译
date: 2018-04-19 15:22:04
tags: [nuttx]
---

&ensp;
<!--more-->

ubuntu下nuttx下载和编译
==============

[参考资料-优酷视频](http://v.youku.com/v_show/id_XMTg2Mzc5NDYxMg.html?spm=a2h0j.11185381.listitem_page1.5!9~A)

----

1. 系统环境配置
    ```bash
    $sudo apt-get install automake bison build-essential flex gcc-arm-none-eabi gperf git libncurses5-dev libtool libusb-dev libusb-1.0-0-dev minicom
    $mkdir openocd
    $cd openocd
    $git clone http://repo.or.cz/r/openocd.git
    $cd openocd
    $./bootstrap
    $./configure --enable-internal-jimtcl --enable-maintainer-mode --disable-werror --disable-shared --enable-stlink --enable-jlink --enable-rlink --enable-vslink --enable-ti-icdi --enable-remote-bitbang
    $make
    $sudo make install
    ```
2. 参考命令
    ```bash
    $mkdir nuttx-os
    $cd nuttx-os
    $git clone https://bitbucket.org/nuttx/nuttx.git nuttx
    $git clone https://bitbucket.org/nuttx/buildroot.git buildroot
    $git clone https://bitbucket.org/nuttx/nonbsd.git nonbsd
    $git clone https://bitbucket.org/nuttx/nxwidgets.git NxWidgets
    $git clone https://bitbucket.org/nuttx/pascal.git Pascal
    $git clone https://bitbucket.org/nuttx/tools.git tools
    $git clone https://bitbucket.org/nuttx/uclibc.git uClibc++
    ```
3. 配置nuttx
    ```bash
    $cd tools
    $cd kconfig-frontends
    $./configure
    $make
    $sudo make install
    $sudo ldconfig
    $cd ../..
    $cd nuttx/
    $cd tools
    $./configure.sh stm32f103-minimum/nsh
    $cd ..
    $make menuconfig
    $make
    $ls -l nuttx.bin
    ```
4. 通过openocd刷入固件
    ```bash
    $cd openocd
    $cd contrib/
    $sudo cp 99-openocd.rules /etc/udev/rules.d/
    $sudo udevadm trigger
    $cd ../..
    $lsusb//查看usb挂载情况
    $dmesg
    $openocd -f interface/stlink-v2.cfg -f target/stm32f7x.cfg //初始化stlink
    $openocd -f interface/stlink-v2.cfg -f target/stm32f7x.cfg //若连接了芯片,可以看出芯片型号
    $openocd -f interface/stlink-v2.cfg -f target/stm32f7x.cfg -c init -c "reset halt" -c "flash write_image erase nuttx.bin 0x08000000" //通过stlink刷入固件
    ```
5. 配置minicom
    ```bash
    $minicom -s
    ```