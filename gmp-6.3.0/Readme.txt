$ tar -xvf gmp-6.3.0.tar.gz
$ cd  gmp-6.3.0
$ ./configure --enable-cxx --host=aarch64-xilinx-linux --prefix=/home/ming/Desktop/gmp/gmp-6.3.0-aarch64.pkg
$ make
$ make install