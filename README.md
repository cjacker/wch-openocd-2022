# Latest source of official WCH OpenOCD (2024-11-26 version)

This repo host the outdated source of WCH OpenOCD **(about 2022 version)**.

- It can work with old version WCH-LinkE firmware if you do not want to update the firmware to latest version.
- Support program / debug WCH ch32v003/103/20x/30x.

**it's highly recommended to update the firmware to latest version and use latest [WCH OpenOCD](https://github.com/cjacker/wch-openocd)**

## Installation

```
./bootstrap
./configure --prefix=/opt/wch-openocd-2022 --enable-wlink --disable-linuxgpiod --disable-werror --program-prefix=wch- --program-suffix=-2022
make
sudo make install
```

After installation successfully, please add `/opt/wch-openocd/bin` to your PATH env, the command is "wch-openocd-2022".

## Usage

```
wch-openocd-2022 -f /opt/wch-openocd/share/openocd/scripts/target/wch-riscv.cfg

```

You may copy `wch-riscv.cfg` to your project dir to avoid use such a long PATH.

