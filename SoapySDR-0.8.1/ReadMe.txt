// load environment for Petalinux
source /opt/petalinux/2020.1/environment-setup-aarch64-xilinx-linux
// Confirm Compiler version
$CC --version
aarch64-xilinx-linux-gcc (GCC) 9.2.0
Copyright (C) 2019 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

// Download Source Code
https://codeload.github.com/pothosware/SoapySDR/zip/refs/heads/master

unzipp SoapySDR-master.zip

cd /home/ming/Downloads/SoapySDR/SoapySDR-master

mkdir build

cd build

cmake .. -DCMAKE_SYSTEM_NAME=Linux \
	  -DCMAKE_SYSTEM_PROCESSOR=aarch64 \
	  -DCMAKE_INSTALL_PREFIX=/home/ming/Downloads/SoapySDR/usr \
	  -DBUILD_SHARED_LIBS=ON \
	  -DBUILD_STATIC_LIBS=OFF \
	  -DBUILD_gflags_nothreads_LIB=OFF
	  
make -j4

sudo make install

