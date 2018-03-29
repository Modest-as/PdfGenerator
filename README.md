# Powered by [libharu](https://github.com/libharu/libharu)

## Windows

### Use NMake and CMake

Install [cmake](https://cmake.org/download/).

`cmake -G "NMake Makefiles" ../libharu`

NMake comes together with Visual Studio so use VS developer console.

After the configuration and creation of the makefile run `nmake` to create
the libraries and demonstrations. By default a shared library will be 
created therefore you need to copy the `libhpdf.dll` from the src directory
in the demo directory in order for the demonstrations to run correctly.

### Useful CMake options

There are some options available where you can influence the configuration
stage. These options must be given at the command line with the `-D` flag, e.g.

`cmake -G "NMake Makefiles" -DCMAKE_BUILD_TYPE=Debug ../libharu`

* `CMAKE_BUILD_TYPE=Debug|Release` - debug or release build
* `BUILD_SHARED_LIBS=ON|OFF` - shared or static build
* `CMAKE_COLOR_MAKEFILE=ON|OFF` - color output
* `CMAKE_VERBOSE_MAKEFILE=ON|OFF` - verbose makefile output

More options can be found [here](http://www.cmake.org/Wiki/CMake_Useful_Variables).

### Example

* `cmake -G "NMake Makefiles" -DCMAKE_BUILD_TYPE=Release -DBUILD_SHARED_LIBS=ON ../`
* `nmake`