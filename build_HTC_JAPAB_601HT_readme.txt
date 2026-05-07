export ARCH=arm64
export SUBARCH=arm64
export CROSS_COMPILE=/home/dinhlongbk/samba/htc_u11_kernel_andorid_9/aarch64-linux-android-4.9/bin/aarch64-linux-android-
make O=out mrproper
# make O=out clean 
make O=out htcperf_defconfig
make O=out -j12


# Japan 601HT
make O=out -j$(nproc) PRIVATE_SKU_NAME=JAPAN
