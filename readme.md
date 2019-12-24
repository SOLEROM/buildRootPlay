# buildRoot build and test

* rnd1: buildroot build fs+kernel+run in qemu (build01-works) 
* rnd2: buildroot build only fs ; kernel build sepetare : run in qemu (build02)

##  buildRoot builds

```
build01	- with kenrel config in menuconfig
build02	- no kenrel config in menuconfig
```

## rnd1

* run test:

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




