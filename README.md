# rpi-toolchain

This repository contains a crosstool-ng configuration file to build a toolchain for the Raspberry Pi Zero W. The
configuration was modified from the one
available [here](https://gist.github.com/h0tw1r3/19e48ae3021122c2a2ebe691d920a9ca) to be more up-to-date with current
releases of Raspbian.

This was necessary as `arm-rpi-linux-gnueabihf-gcc` will embed ARM Thumb code when linking to libc which is not
supported by the Raspberry Pi Zero W processor,
see [here](https://stackoverflow.com/questions/46276917/how-to-compile-arm32-only-binary-no-thumb). This toolchain
produces 100% non-thumb ARM assembly.

This toolchain is mainly used to build Raspberry compatible builds
of [go-librespot](https://github.com/devgianlu/go-librespot).