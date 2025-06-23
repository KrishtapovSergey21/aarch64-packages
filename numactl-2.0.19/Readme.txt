$ sudo apt-get install autoconf automake libtool
$ autoreconf --install --force
$ tar -xvf numactl-2.0.19.tar.gz
$ cd  numactl-2.0.19
$ ./configure --host=aarch64-xilinx-linux --prefix=/home/ming/Desktop/numactl-2.0.19-aarch64.pkg
$ make
$ make install
