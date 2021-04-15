WiringPi (Unofficial Mirror/Fork)
=================================

This is an unofficial mirror/fork of wiringPi to support ports (Python/Ruby/etc).  With the
[end of official development](http://wiringpi.com/wiringpi-deprecated/), this repository
has become a mirror of the last "official" source release, plus a fork facilitating updates
to support newer hardware (primarily for use by the ports) and fix bugs.

  * The final "official" source release can be found at the
    [`final_source_2.50`](https://github.com/WiringPi/WiringPi/tree/final_official_2.50) tag.
  * The default `master` branch contains code that has been written since that final source
    release to provide support for newer hardware.

Install 安装
-----
Download from the last Releases.

从Releases下载最新的构建文件。

https://github.com/guation/WiringPi-arm64/releases

`sudo apt install -f ./wiringpi-*-g.deb`

Build 构建
-----
```
git clone https://github.com/guation/WiringPi-arm64.git
cd WiringPi-arm64/
```
build for install,not recommended. 直接安装(仅编译安装对应架构的库文件，不推荐)。

`./build`

build for deb,recommend. 打包deb(同时编译32位和64位库，可以兼容依赖32位库构建的应用程序，推荐)。

```
sudo apt install -y gcc-arm-linux-gnueabihf
./build debian
sudo apt install -fy ./debian-template/wiringpi-`cat VERSION`.deb
```


Ports
-----

wiringPi has been wrapped for multiple languages:

* Node - https://github.com/WiringPi/WiringPi-Node
* Perl - https://github.com/WiringPi/WiringPi-Perl
* PHP - https://github.com/WiringPi/WiringPi-PHP
* Python - https://github.com/WiringPi/WiringPi-Python
* Ruby - https://github.com/WiringPi/WiringPi-Ruby

Support
-------

Please do not email Gordon if you have issues, he will not be able to help.

Pull-requests may be accepted to add or fix support for newer hardware, but new features or
other changes may not be accepted.

For support, comments, questions, etc please join the WiringPi Discord channel: https://discord.gg/SM4WUVG
