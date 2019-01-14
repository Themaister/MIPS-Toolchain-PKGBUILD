# MIPS toolchains

This repo contains some nifty Arch Linux PKGBUILDs to build MIPS toolchains for both little- and big-endian.

Build in order for your target endianness.

- binutils
- gcc-stage1 (bootstrap GCC)
- linux-api-headers
- glibc
- gcc (full compiler). It conflicts with -stage1, gcc will replace it when you install it.

For little-endian:

```
mipsel-linux-gnu-gcc -o test test.c -static -O3 -march=mips1
```

Big-endian:

```
mips-linux-gnu-gcc -o test test.c -static -O3 -march=mips1
```
