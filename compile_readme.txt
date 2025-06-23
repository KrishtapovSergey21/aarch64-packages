// Gflags
// ChatGPT cross-compile alsa source code under Petalinux 2020.1
// load environment for Petalinux
source /opt/petalinux/2020.1/environment-setup-aarch64-xilinx-linux

// Confirm Compiler version
$CC --version

aarch64-xilinx-linux-gcc (GCC) 9.2.0
Copyright (C) 2019 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

// Download and install a library
wget https://github.com/gflags/gflags/archive/v2.2.2.tar.gz
tar xvf gflags-v2.2.2.tar.gz
cd gflags-2.2.2/
cmake -DCMAKE_SYSTEM_NAME=Linux \
	  -DCMAKE_SYSTEM_PROCESSOR=aarch64 \
	  -DCMAKE_INSTALL_PREFIX=/opt/petalinux/2020.1/sysroots/aarch64-xilinx-linux
	  -DBUILD_SHARED_LIBS=ON \
	  -DBUILD_STATIC_LIBS=OFF \
	  -DBUILD_gflags_nothreads_LIB=OFF  ..
make
sudo make install

// On here
cmake -DCMAKE_SYSTEM_NAME=Linux \
	  -DCMAKE_SYSTEM_PROCESSOR=aarch64 \
	  -DCMAKE_INSTALL_PREFIX=/opt/petalinux/2020.1/sysroots/aarch64-xilinx-linux
	  
***It's default configuration, and other parameters depends on source library.

