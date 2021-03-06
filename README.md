# ![SnowFlake](./logo.png)

[![BSD-3-Clause][s1]][li]

[s1]: https://img.shields.io/badge/License-BSD%203--Clause-blue.svg

[li]: LICENSE

Technology is free, SnowFlakeOS

## TODO
### Boot2Snow (x86_64, UEFI)
- [x] Basical UI (from https://github.com/system76/firmware-update)
- [x] Load kernel from disk
### SnowKernel (ExoKernel)
- [ ] Load kernel as higher half (0xffffffff80000000)
- [ ] Better GUI library support
- [ ] Write I/O drivers (keyboard, mouse, etc.)
- [ ] Multitasking support
- [ ] Write syscall
- [ ] Write init process
### FlakeOS (LibOS)

## Building
This is SnowFlake is require for build.
- Rust (https://www.rust-lang.org)
- NASM (http://www.nasm.us/)
- GCC Toolchain or GCC (https://gcc.gnu.org/)

### Windows
Will be added later

### Mac
macOS is default ld is bsd ld (cannot link SnowFlake)
and default as is clang too (build error)
If you want build SnowFlake on macOS
- Need HomeBrew (https://brew.sh/)
- Need Xcode Command Line Tools (This will install both HomeBrew)
- Need NASM (can install in HomeBrew)
- Need QEMU (if you want run SnowFlake)
```
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
$ homebrew install nasm qemu crystal
$ git clone https://github.com/SnowFlake/mac-binutils-script.git
$ cd mac-binutils-script
$ sudo ./compile.sh
$ git clone https://github.com/SnowFlake/SnowFlake.git
$ cd SnowWhite
$ make run
```

### Linux
To build SnowFlake as an x86_64 target, x86_64-elf cross-compilation is required.
If you do not have the x86_64-elf compiler, and your system is x86_64, you can use the 'x86_64-linux_env.sh' script.
```
$ sh x86_64-linux_env.sh
```
#### Arch Linux
```
$ pacman -S qemu nasm mtools
$ git clone https://github.com/SnowFlake/SnowFlake.git
$ cd SnowWhite
$ make run
```

## Thanks to
- https://github.com/phil-opp/blog_os
- https://github.com/beevik/MonkOS
- https://github.com/thepowersgang/rust_os
- https://github.com/wichtounet/thor-os
- https://github.com/anchovieshat/cathode
- https://github.com/TheKernelCorp/NuummiteOS
- https://github.com/redox-os/orbclient
- https://github.com/redox-os/uefi
- https://github.com/system76/firmware-update
