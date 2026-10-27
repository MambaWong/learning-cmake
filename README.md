learning-cmake
==============

This is a simple CMake practice repository containing several independent examples.

Each example has its own `CMakeLists.txt`; configure and build it from the repository root
with CMake's `-S` and `-B` options. For example:

```sh
cmake -S hello-world -B build/hello-world
cmake --build build/hello-world
```

The build directory is kept separate from the source directory.

## Examples

* `hello-world`: the simplest executable.
* `hello-world-clear`: separates source files and demonstrates install rules.
* `hello-world-lib`: builds static and shared versions of a library.
* `hello-world-shared`: links an executable against a separately built library.
* `curl`: finds and links the system libcurl library; libcurl development files must be installed.
* `hello-module`: demonstrates finding a library with a custom CMake find module.

[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/Akagi201/learning-cmake/trend.png)](https://bitdeli.com/free "Bitdeli Badge")
