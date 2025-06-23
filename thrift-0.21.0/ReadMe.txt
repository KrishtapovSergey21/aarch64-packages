tar xvf thrift-0.21.0.tar.xz
cd thrift-0.21.0
sudo autoreconf -i
sudo ./configure --host=aarch64-xilinx-linux --prefix=/home/ming/Desktop/Work/thrift-0.21.0-aarch64.pkg/usr
sudo make
sudo make install