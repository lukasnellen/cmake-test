# Library sub-project

This is an installable project that builds, installs, and exports several 
libraries. The targets in this project are automatically available to other 
sub-projects when included from the parent directory. This project can also 
be build and installed individually. In that case, it also exports the library
targets through a `cmakeLibConfig.cmake` file. The file gets installed in 
`<prefix>/share/cmake/cmakeLib`, which is one of cmake's standard search 
locations.

Remember to set the `CMAKE_INSTALL_PREFIX`, e.g.,
```
  cmake . -DCMAKE_INSTALL_PREFIX=../install
```
and `make` and `make install` so it can be used by a dependent project. 

A dependent project should set `CMAKE_PREFIX_PATH` (preferred) or `cmakeLib_DIR`
so 
```cmake
  find_package(cmakeLib)
```
can find the package and configure the exported targets. The library targets are
set up so they also provide the information where to find the header files, no
extra include directories have to be configured.
