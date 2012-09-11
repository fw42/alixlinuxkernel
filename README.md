alix3d3 Linux kernels
=====================

This repository contains my Debian packages and .config files of
Linux kernels for my
[PC Engines Alix 3d3 embedded system](http://pcengines.ch/alix.htm).

For me, all of the alix hardware works flawless (except the
watchdog and the GPIO, I never tested those), including USB,
audio, VGA, LEDs, temperature sensors, and the crypto-accelerator.

Debian packages were compiled via

    DEB_HOST_ARCH=i386 ARCH=i386 CONCURRENCY_LEVEL=4 make-kpkg \
    --initrd --us --uc --cross-compile - --arch=i386 --revision=1 \
    --arch-in-name kernel_image

No guarantee for anything. Use at own risk.
