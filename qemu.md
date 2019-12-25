

# buildroot build rootFs+kernel and run qemu

rootfs:  ext2  + kernel: bzImage

```
KERNEL="bzImage"
ROOTFS="rootfs.ext2"

qemu-system-x86_64 \
-kernel $KERNEL \
-drive file=$ROOTFS \
-append "root=/dev/sda rw console=ttyS0" \
-m 128 \
-nographic


```



rootfs: img + kernel: bzImage

```
TBD

```

## run Qemu with dbg options:

```
TBD
```


