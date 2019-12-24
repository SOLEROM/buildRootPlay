# build01

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

