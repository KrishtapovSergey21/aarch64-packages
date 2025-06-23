tar xvf libiio-0.26.tar.gz
cd libiio-0.26

sudo tar xvf libusb-1.0.27-aarch64.pkg.tar.xz  -C /opt/petalinux/2020.1/sysroots/aarch64-xilinx-linux/


mkdir build
cd build
#change CMakeLists.txt
At line 411 remove libxml2
Replace codes from line 412 to line 415 with this code, remove if-else condition.
set(LIBXML2_FOUND ON)
set(LIBXML2_INCLUDE_DIR /opt/petalinux/2020.1/sysroots/aarch64-xilinx-linux/usr/include/libxml2)
set(LIBXML2_LIBRARIES /opt/petalinux/2020.1/sysroots/aarch64-xilinx-linux/usr/lib/libxml2.so)
#######################


cmake -DCMAKE_SYSTEM_NAME=Linux   -DCMAKE_SYSTEM_PROCESSOR=aarch64   -DCMAKE_INSTALL_PREFIX=/home/ming/Desktop/libiio-0.26/libiio-0.26-aarch64.pkg ..

make
make install


