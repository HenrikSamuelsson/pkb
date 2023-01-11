# Sysroot

A sysroot is a scaled down version of your target’s filesystem, it need only contain the libraries and headers which you will compile/link against. In other words sysroot is a directory which is considered to be the root directory for the purpose of locating headers and libraries.

For example if your build toolchain wants to find `/usr/include/foo.h` but you are cross-compiling and the appropriate `foo.h` is in `/my/other/place/usr/include/foo.h`, you would use `/my/other/place` as your sysroot.

The GCC family of compilers accept a `--sysroot=dir` argument, which is used to specify the path to your sysroot.

The CMAKE_SYSROOT content is passed to the compiler in the `--sysroot flag`, if supported.
