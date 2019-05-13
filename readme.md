# Linux Compilation and Boot Process
This repository describe how to compile bootloader, linux kernel and busybox to Raspberry Pi and BeagleBone.

## Toolchain
First, it's necessary to prepare the environment to perform the arm cross compilation. To do so, download Linaro arm toolchain (ex. ``i686_arm-linux-gnueabihf.tar.xz`` for 32bit machine or ``x86_64_arm-linux-gnueabihf.tar.xz`` for 64bit machine ) [here](https://releases.linaro.org/components/toolchain/binaries/latest-7/arm-linux-gnueabihf/).

After download, export the path of the cross compilation toolchain in **.bashrc** including the following line in the end of the file.
```
export PATH=$PATH:<YOUR_EXTRACT_PATH>/gcc-linaro-<VERSION>_arm-linux-gnueabihf/bin
```
And run the command bellow to source the file.
```
source .bashrc
```

To test the cross compiler run the command bellow and check the version installed.
```
gcc --version
```
It is necessary to install the following dependencies too:
```
sudo apt-get install bison flex libssl-dev
```



## BeagleBone
- [Compilations](https://github.com/thalestas/boot-and-compile-process/blob/master/beaglebone/bb.md) - Describe BeagleBone U-boot, Linux Kernel and BusyBox compilations.

## Raspberry Pi
- [Compilations](https://github.com/thalestas/boot-and-compile-process/blob/master/raspberry/rasp.md) - Describe Raspbeery Pi U-boot, Linux Kernel and BusyBox compilations.
