################################################################################
1. Download and unzip the kernel source of G988BXXUFGVJE.

2. Unzip and update the kernel source of  G988BXXUFGVL5.

1. How to Build
        - get Toolchain
                From android git server, codesourcery and etc ..
                - gcc-cfp/gcc-cfp-jopp-only/aarch64-linux-android-4.9/bin/aarch64-linux-android-
        - edit Makefile
                edit "CROSS_COMPILE" to right toolchain path(You downloaded).
                        EX)  CROSS_COMPILE=<android platform directory you download>/android/prebuilts/gcc-cfp/gcc-cfp-jopp-only/aarch64-linux-android-4.9/bin/aarch64-linux-android-
                        EX)  CROSS_COMPILE=/usr/local/toolchain/gcc-cfp/gcc-cfp-jopp-only/aarch64-linux-android-4.9/bin/aarch64-linux-android- // check the location of toolchain
        - to Build
                $ export PLATFORM_VERSION=11
                $ export ANDROID_MAJOR_VERSION=r
                $ export ARCH=arm64
                $ export SEC_BUILD_CONF_VENDOR_BUILD_OS=13
                $ make exynos9830-c1slte_defconfig
                $ make exynos9830-c2sxxx_defconfig
                $ make exynos9830-x1slte_defconfig
                $ make exynos9830-x1sxxx_defconfig
                $ make exynos9830-y2slte_defconfig
                $ make exynos9830-y2sxxx_defconfig
                $ make exynos9830-z3sxxx_defconfig
                $ make

2. Output files
        - Kernel : arch/arm64/boot/Image
        - module : drivers/*/*.ko

3. How to Clean
        $ make clean
################################################################################
