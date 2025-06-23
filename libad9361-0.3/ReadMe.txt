tar xvf libad9361-iio-0.3.tar.gz
cd libad9361-iio-0.3 

sudo tar xvf libiio-0.26-aarch64.pkg.tar.xz  -C /opt/petalinux/2020.1/sysroots/aarch64-xilinx-linux/


mkdir build
cd build

cmake -DCMAKE_SYSTEM_NAME=Linux \
	  -DCMAKE_SYSTEM_PROCESSOR=aarch64 \
	  -DCMAKE_INSTALL_PREFIX=/home/ming/Desktop/libad9361-0.3/libad9361-0.3-aarch64.pkg \
	  -DLIBIIO_INCLUDEDIR=/opt/petalinux/2020.1/sysroots/aarch64-xilinx-linux/usr/include \
	  -DLIBIIO_LIBRARIES=/opt/petalinux/2020.1/sysroots/aarch64-xilinx-linux/usr/lib/libiio.so ..

make
make install


