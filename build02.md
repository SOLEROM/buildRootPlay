# build02


## buildRoot


## buildKernel

```
gitsrc 
https://kernel.googlesource.com/pub/scm/linux/kernel/git/next/linux-next.git

sudo make clean
sudo mkdir kernelBuildFiles
sudo make O=./kernelBuildFiles ARCH=x86_64 x86_64_defconfig
sudo make O=./kernelBuildFiles ARCH=x86_64 menuconfig
sudo make O=./kernelBuildFiles ARCH=x86_64 -j 4 bzImage



```

## test Run

```
KERNEL="bzImage"
ROOTFS="rootfs.ext4"

sudo qemu-system-x86_64 \
-kernel $KERNEL \
-boot c -m 2049M \
-hda $ROOTFS \
-append "root=/dev/sda rw console=ttyS0 " \
-nographic

```
