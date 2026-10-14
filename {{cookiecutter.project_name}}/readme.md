# {{cookiecutter.project_name}}

# Build

This application can be built on Windows with Visual Studio compiler or MinGW compiler and on Linux with gcc compiler.

## Windows

### Visual Studio

Install Qt (https://www.qt.io/development/download-qt-installer-oss)

Build (x64 Native Tools Command Prompt for VS 20XX)
```bash
cmake -G Ninja -DCMAKE_BUILD_TYPE=Release -B Release -DCMAKE_PREFIX_PATH=path/to/qt
cmake --build Release
```

### MinGW (MSYS2)

Install compiler, tools and libraries (MSYS2 UCRT64)
```bash
pacman -S mingw-w64-ucrt-x86_64-gcc mingw-w64-ucrt-x86_64-cmake make mingw-w64-ucrt-x86_64-ninja mingw-w64-ucrt-x86_64-qt6-base
```

Build (MSYS2 UCRT64)
```bash
cmake -G Ninja -DCMAKE_BUILD_TYPE=Release -B Release
cmake --build Release
```

## Linux (Ubuntu, Debian)

Install compiler, tools and libraries
```bash
sudo apt install build-essential cmake ninja-build qt6-base-dev
```

Build
```bash
cmake -G Ninja -DCMAKE_BUILD_TYPE=Release -B Release
cmake --build Release
```