---
layout: post
title: Kernel Level Hooking
subtitle: System Call Hooking with Kernel Modules
---

OWASP MASTG 문서를 보던 중 커널 레벨에서 후킹하는 방법이 기술되어 있어 분석 및 PoC를 진행해보았다. Frida라는 강력한 도구가 있기 때문에 이 Hooking 기법이 많이 사용되진 않을 것으로 생각이 되어진다.

OWASP MASTG 에서는 커널 레벨 후킹을 통해 특정 파일을 은닉하는 방법을 예제로 기술해놓았는데, 루팅 탐지 우회에 사용할 수 있을 것 같다.

(앱이 무결성 검증과 Frida 탐지를 하고 있고 이를 정말정말정말 우회하기 힘들거나 귀찮은 경우에나 사용할 수 있으려나,,)

### Windows 플랫폼에서 ARM Linux 크로스 컴파일 환경 구성하기

https://developer.moe/linux-cross-compile-toolchain-on-cygwin#cygwin-install

adb shell getprop | findstr abi
[ro.product.cpu.abi]: [x86]
[ro.product.cpu.abilist]: [x86,armeabi-v7a,armeabi]
[ro.product.cpu.abilist32]: [x86,armeabi-v7a,armeabi]
[ro.product.cpu.abilist64]: []

1) Arm GNU Toolchain Downloads
https://developer.arm.com/downloads/-/arm-gnu-toolchain-downloads
Windows (mingw-w64-i686) hosted cross toolchains
arm-gnu-toolchain-13.2.rel1-mingw-w64-i686-arm-none-linux-gnueabihf.zip
unzip

2) cmake Downloads
https://cmake.org/download/
Binary distributions: Windows x64 ZIP
cmake-3.28.0-rc5-windows-x86_64.zip
unzip

3) install GNU make 
https://sourceforge.net/projects/mingw/files/Installer/
mingw-get-setup.exe
All Packages > mingw32-make (Class=bin) > Mark for installation
Installation > Apply Changes



To be honest, I'm having some trouble remembering right now, so why don't you just watch [my movie](https://en.wikipedia.org/wiki/The_Princess_Bride_%28film%29) and it will answer **all** your questions.
