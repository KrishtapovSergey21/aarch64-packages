tar xvf matio-1.5.28.tar.xz
cd matio-1.5.28
autoreconf -i
./configure --host=aarch64-xilinx-linux --prefix=/home/ming/Desktop/Work/matio-1.5.28-aarch64.pkg/usr
sudo make
sudo make install