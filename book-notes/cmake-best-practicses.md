---
tags: cmake
---
# Book Notes - CMake Best Practices

## Chapter 1 - Kickstarting CMake

### CMake In A Nutshell

CMake is cross-platform free and open-source tool set for build automation, testing, packaging and installation of software. It is also compiler-independent which is a benefit to build and distribute cross-platform software.

CMake includes the following three command-line tools:

- `cmake`: CMake itself, used to generate build instructions
- `ctest`: CMake's test utility, used to detect an run tests
- `cpack`: CMake's packaging tool, used to pack software into install files

### Building CMake From Source

The book explains how to build CMake from source. I did not try this and instead downloaded a file called Windows x64 Installer from the [cmake.org download page](https://cmake.org/download/).

Made the following choices when running the CMake installer:

- Add CMake to the system PATH for all users
- Set destination folder to C:\tools\cmake

The reason for changing the folder where CMake is to be installed is due to that the default folder was Program Files, a folder name that contains a space. A space in a path can be problematic and might causes issues later on when using CMake. It is best practices to avoid spaces in both paths and file names.

### Building Your First Project

The book is accompanied by a GitHub repository [CMake-Best-Practices](https://github.com/PacktPublishing/CMake-Best-Practices) that I cloned on to my Windows PC.

Built a first project by use of commands in a terminal, as shown below, starting out at the root of the cloned repository. Note that output of commands are omitted.

```txt
cd chapter01
mkdir build
cd build
cmake ..
cmake --build .
```

This produced an executable called `chapter1.exe` found in the subfolder `\simple_executable\Debug\`.

Executed the newly built program with this command:

```txt
.\simple_executable\Debug\chapter1.exe
```

Execution caused the following output:

```txt
Welcome to CMake Best Practices
```

A typical file structure for for a CMake project looks like this:

```txt
.
|- CMakeLists.txt
|- build\
|- src\
```

The file `CMakeLists.txt` contains instructions for CMake on how to create build instructions for the project. A CMake project requires this file at the root of the project and there can be additional files with this name in various subfolders.

The `build` folder is used for output produced by CMake when running the build. If building an executable so will this end up in a subfolder under this folder.

The `src` folder holds source code that forms the input when building with CMake. This can be a set of C or C++ source files to be compiled.

## Understanding the CMake Build Process

CMake uses a two step build process split into a configuration and build phase, and the first configuration phase is further split into two phases;configure and generate:

- Configuration
  - Configure
    - Parse CMakeLists.txt
    - Detect toolchains
    - Detect the architecture
    - Find dependencies
    - Generate cache
  - Generate
    - Write build tool files
    - Generate the cache
- Build
  - Compile binaries
  - Link binaries
  - Run tests
  - Pack artifacts
