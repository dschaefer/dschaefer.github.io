---
layout: post
title: QNX CMake Toolchain File
date: '2017-10-06 15:03:57'
tags:
- qnx
- cmake
---

I've been using CMake for some internal projects at QNX and have fallen in love with it. CMake's support for multiple build outputs and inter component dependency management makes it a natural for BSP projects. And when combined with Ninja, it's very fast, especially on Windows.

CMake has upstream support for our compiler driver qcc. All you need is a toolchain file to hook everything up. Instructions on how to use the file are available in CMake's docs here:

https://cmake.org/cmake/help/latest/manual/cmake-toolchains.7.html

The contents of the file I use is included below. The example is for x86_64 available in SDP7.

```
set(CMAKE_SYSTEM_NAME QNX)

set(arch gcc_ntox86_64)
set(ntoarch x86_64)
set(QNX_PROCESSOR x86_64)

set(CMAKE_C_COMPILER qcc)
set(CMAKE_C_COMPILER_TARGET ${arch})

set(CMAKE_CXX_COMPILER qcc -lang-c++)
set(CMAKE_CXX_COMPILER_TARGET ${arch})

set(CMAKE_ASM_COMPILER qcc -V${arch})
set(CMAKE_ASM_DEFINE_FLAG "-Wa,--defsym,")

set(CMAKE_RANLIB $ENV{QNX_HOST}/usr/bin/nto${ntoarch}-ranlib
    CACHE PATH "QNX ranlib Program" FORCE)
set(CMAKE_AR $ENV{QNX_HOST}/usr/bin/nto${ntoarch}-ar
    CACHE PATH "QNX qr Program" FORCE)
```

To use with other architectures, you just need to change the arch section. For example, this is what I use for ARMv7.

```
set(arch gcc_ntoarmv7le)
set(ntoarch armv7)
set(QNX_PROCESSOR armle-v7)
```

We'll contribute this to the CMake help docs once we're happy with it. We also need to contribute a few changes to support the ASM assember stuff. It works but gives an ugly warning.

Please let me know in the comments if this works for you or if you have any issues with it. I'll update this page as we find better ways to do things.