# build01

## build

```
build.sh
========
#!/bin/bash
project="/proj/theKernel/kernelRootBuild"
buildRootFs="$project/buildRoot2019/buildroot-2019.02.8"
buildRootFs_config="$buildRootFs/.config"

cd $buildRootFs
make defconfig
sudo make menuconfig
sudo make

echo "buildRootConfigFile = $buildRootFs_config"
```


## run test:

```
run build1 qemu works:
======================
KERNEL="bzImage"
ROOTFS="rootfs.ext2"

qemu-system-x86_64 \
-kernel $KERNEL \
-drive file=$ROOTFS \
-append "root=/dev/sda rw console=ttyS0" \
-m 128 \
-nographic

```

