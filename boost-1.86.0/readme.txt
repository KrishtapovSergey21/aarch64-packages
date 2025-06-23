// load environment for Petalinux
source /opt/petalinux/2020.1/environment-setup-aarch64-xilinx-linux
// Confirm Compiler version
$CC --version
aarch64-xilinx-linux-gcc (GCC) 9.2.0
Copyright (C) 2019 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

// Boost 1.88.0 compiling error
CMake Error at libs/lockfree/CMakeLists.txt:45 (set_target_properties):
  INTERFACE_LIBRARY targets may only have whitelisted properties.  The
  property "CMAKE_CXX_STANDARD_REQUIRED" is not allowed.


// Download Source Code
https://github.com/boostorg/boost/releases/download/boost-1.86.0/boost-1.86.0-cmake.tar.gz

unzipp pugixml-1.15.tar.gz

cd /home/ming/Downloads/boost/boost-1.86.0

mkdir build

cd build

cmake .. -DCMAKE_SYSTEM_NAME=Linux \
	  -DCMAKE_SYSTEM_PROCESSOR=aarch64 \
	  -DCMAKE_INSTALL_PREFIX=/home/ming/Downloads/boost/usr \
	  -DBUILD_SHARED_LIBS=ON \
	  -DBUILD_STATIC_LIBS=OFF \
	  -DZLIB_ROOT=/opt/petalinux/2020.1/sysroots/aarch64-xilinx-linux/usr \
	  -DOPENSSL_ROOT_DIR=/opt/petalinux/2020.1/sysroots/aarch64-xilinx-linux/usr
	  
make -j4

sudo make install

