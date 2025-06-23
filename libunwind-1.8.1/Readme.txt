$ tar -xvf libunwind-1.8.1.tar.gz
$ cd  libunwind-1.8.1
$ autoreconf -i 
$ ./configure --host=aarch64-xilinx-linux --prefix=/home/ming/Desktop/libunwind/libunwind-1.8.1-aarch64.pkg
$ make
$ make install

