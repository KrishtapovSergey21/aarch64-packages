tar xvf libaio-0.3.113.tar.gz
cd libaio-0.3.113
 make CC="aarch64-xilinx-linux-gcc --sysroot=/opt/petalinux/2020.1/sysroots/aarch64-xilinx-linux"
 make  install DESTDIR=/home/ming/Desktop/libaio-0.3.113/libaio-0.3.113-aarch64.pkg
