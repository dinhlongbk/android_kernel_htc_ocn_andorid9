


# set env
export GCC_BIN=/home/dinhlongbk/samba/lineage_os/prebuilts/gcc/linux-x86/aarch64/aarch64-linux-android-4.9/bin
export PATH="$GCC_BIN:$PATH"
export ARCH=arm64
export SUBARCH=arm64
export CROSS_COMPILE=aarch64-linux-android-

# build
make O=out htcperf_defconfig
make -j$(nproc --all) O=out

# build for JAPAN 601HT
make O=out -j$(nproc) PRIVATE_SKU_NAME=JAPAN