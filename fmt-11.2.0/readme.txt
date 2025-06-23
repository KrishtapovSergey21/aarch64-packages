// load environment for Petalinux
source /opt/petalinux/2020.1/environment-setup-aarch64-xilinx-linux

cd /opt/petalinux/2020.1/sysroots/aarch64-xilinx-linux

// Confirm Compiler version
$CC --version

aarch64-xilinx-linux-gcc (GCC) 9.2.0
Copyright (C) 2019 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

cd fmt-11.2.0

cmake -DCMAKE_SYSTEM_NAME=Linux \
	  -DCMAKE_SYSTEM_PROCESSOR=aarch64 \
	  -DCMAKE_INSTALL_PREFIX=/home/ming/Desktop/bond/fmt-11.2.0/fmt-11.2.0.-aarch64.pkg/usr

make PREFIX=/home/ming/Desktop/bond/fmt-11.2.0/fmt-11.2.0.-aarch64.pkg/usr
sudo make install PREFIX=/home/ming/Desktop/bond/fmt-11.2.0/fmt-11.2.0.-aarch64.pkg/usr