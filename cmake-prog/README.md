# Executable sub-project

A simple executable that uses the libraries from the library sub-project.

To setup up as a stand-alone project, set the `CMAKE_PREFIX_PATH` environment 
variable before invoking `cmake`, e.g., 

```
  export CMAKE_PREFIX_PATH=../../cmake-lib/install
  cmake .
```
