# floppy shooter

A linux port of [floppy shooter](https://github.com/ILBBBM2/floppy-shooter), a 3d game that will fit on a formatted floppy disk, by [ILBBBM2](https://github.com/ILBBBM2)

## usage

download and extract the compressed folder and run the `main` executable file

## compatibility

floppy shooter should work on any 64-bit linux distribution, along with the following requirements as originally stated

> - processor: 2ghz+ clock (core duo)
> - ram: 128mb or greater
> - graphics card: 3dfx Voodoo Graphics 4 MB +
> - os: ~~windows xp 64bit+~~ linux (debian 12)
> - storage: 1.25mb

release builds are tested on debian 12 64-bit with wayland

## build

release builds are built with gcc and a static build of raylib, then compressed with upx

### gcc

the following options are passed to gcc

```text
-g0 -Oz -s -fno-asynchronous-unwind-tables -fno-ident -static-libgcc -static-libstdc++ 
```

`-static` is not passed to gcc because of libraries that are hard to statically link

however, the number of dynamic libraries linked is minimal and should be extremely compatible

### upx

the following options are passed to upx

```text
--best --ultra-brute
```

this allows for maximal compression

## credits

thank you to [ILBBBM2](https://github.com/ILBBBM2) for creating the game
