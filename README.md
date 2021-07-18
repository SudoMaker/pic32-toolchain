# pic32-toolchain
Relatively new toolchain for PIC32 MCUs.

## Components
#### GCC
Version: 11.1.0

Build options: `../gcc-11.1.0/configure --target mipsel-elf --prefix=/build/pic32-toolchain/out --disable-nls --disable-shared --with-newlib --with-headers=./../newlib-4.1.0/newlib/libc/include --enable-languages=c,c++ CFLAGS='-O2' CXXFLAGS='-O2'`

#### binutils
Version: 2.36

Build options: `./configure --target mipsel-elf --prefix=/build/pic32-toolchain/out CFLAGS='-O2' CXXFLAGS='-O2'`

#### GDB
Version: 10.2

Build options: `../gdb-10.2/configure --target mipsel-elf --prefix=/build/pic32-toolchain/out CFLAGS='-O2' CXXFLAGS='-O2'`

### newlib
Version: 4.1.0

Build options: `../newlib-4.1.0/configure --target mipsel-elf --prefix=/build/pic32-toolchain/out CFLAGS='-O2' CXXFLAGS='-O2'`

### pic32m-bin2hex
**This is a non-free component made by Microchip.**

## Dowloads
See the releases section.

Currently only supports Linux x86_64.

## Notes
You need external crt0.S and linker scripts for this thing to work. See [PIC32_CMake](https://github.com/SudoMaker/PIC32_CMake) for an example.
