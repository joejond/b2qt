## What's this

Boot to Qt (b2qt) is the reference distro used in [Qt for Device Creation](https://www.qt.io/qt-for-device-creation/). It combines Poky, meta-qt5 and various BSP meta layers to provide an integrated solution for building device images and toolchains with the latest Qt version.

This repository is used to extend b2qt to support new devices and features .

## How to build

To initialize build environment, use the b2qt-init-build-env script.

Usage: b2qt-init-build-env COMMAND [ARGS]
> To get more information, Please refer to [Building Your Own Embedded Linux Image](http://doc.qt.io/QtForDeviceCreation/qtee-custom-embedded-linux-image.html)

### Setting Up Yocto Build Environment

For example:

  `b2qt-init-build-env init raspberrypi3`

List available devices:

  `b2qt-init-build-env list-devices`

### Building the Image and Toolchain

```
export MACHINE=raspberrypi3
source ./setup-environment.sh

bitbake b2qt-embedded-qt5-image
bitbake meta-toolchain-b2qt-embedded-qt5-sdk
```

