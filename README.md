# Debian Build for AllWinner H616

## Tested Hardwares

* [Yuzuki Chameleon](https://github.com/YuzukiHD/YuzukiChameleon)
  - XR829 wireless module driver is not added yet. We are working on this.
  
* [BigTreeTech CB1](https://github.com/bigtreetech/CB1)

## Build Prerequisites

On Ubuntu22.04

``` zsh
sudo apt install -y ccache debian-archive-keyring debootstrap device-tree-compiler dwarves
sudo apt install -y gcc-arm-linux-gnueabihf jq libbison-dev libc6-dev-armhf-cross
sudo apt install -y libelf-dev libfl-dev liblz4-tool libpython2.7-dev libusb-1.0-0-dev
sudo apt install -y pigz pixz pv swig pkg-config python3-distutils qemu-user-static u-boot-tools
sudo apt install -y distcc uuid-dev lib32ncurses-dev lib32stdc++6 apt-cacher-ng
sudo apt install -y aptly aria2 libfdt-dev libssl-dev
```

## Versions Included

|  Part  | Version  |
| :----: | :------: |
| uboot  | v2021.10 |
| kernel | v5.16.17 |

## Project Build

In the project's root directory, run:

``` bash
sudo ./build.sh
```

- uboot config file
    
    Allwinner-H616/u-boot/configs/h616_defconfig

- Compile information output directory

    output/debug/

## Reference

- Allwinner usb boot: https://linux-sunxi.org/FEL/USBBoot

- [Allwinner Online Development Forum](https://bbs.aw-ol.com/topic/2054/mq-quad-h616-%E4%B8%BB%E7%BA%BF%E5%86%85%E6%A0%B8%E7%BC%96%E8%AF%91%E8%B0%83%E8%AF%95%E8%AE%B0%E5%BD%95-u-boot-kernel-buildroot/17)

