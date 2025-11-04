# How to Compile
1. Download Toolchains:
[GCC 7.3](https://github.com/Teamlions/aarch64-linux-gnu-7.3)  
you also have to find & install `arm-none-eabi-gcc`, it is used for compiling compact vDSO. I'd installed it with my package manager

```sh
export PATH="~/kernel-stuffs/cross-compiler/gcc/bin:$PATH"
export ARCH=arm64
export CROSS_COMPILE=aarch64-linux-gnu-
export CLANG_TRIPLE=aarch64-linux-gnu-
export CROSS_COMPILE_ARM32=arm-none-eabi-
```
`mkdir -p out`  
`make O=out clean`  
`make O=out mrproper`  
`make O=out X00TD_defconfig`  
`make O=out -j$(nproc --all) KCFLAGS=-Wno-error`  
or  
`make O=out KCFLAGS=-Wno-error`  

`-Wno-error` flag is import, otherwise Qualcomm’s QCACLD-3.0 Wi-Fi driver will fail compiling.
