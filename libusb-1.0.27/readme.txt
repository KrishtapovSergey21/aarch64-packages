- generate configure from configure.ac
	autoreconf -i
- configuration and build
	./configure --host=aarch64-xilinx-linux --prefix=/home/ming/Desktop/itplayer/libusb/usr
	make install