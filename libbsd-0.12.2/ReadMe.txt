tar xvf libbsd-0.12.2.tar.xz
cd libbsd-0.12.2
sudo tar xvf libmd-1.1.0-aarch64.pkg.tar.xz -C /opt/petalinux/2020.1/sysroots/aarch64-xilinx-linux/

autoreconf -fi

./configure --host=aarch64-xilinx-linux --prefix=/home/ming/Desktop/libbsd-0.12.2/libbsd-0.12.2-aarch64.pkg

make
make install

