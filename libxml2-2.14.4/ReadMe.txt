https://download.gnome.org/sources/libxml2/2.14/libxml2-2.14.4.tar.xz

tar xvf libxml2-2.14.4.tar.xz
cd libxml2-2.14.4
./configure --host=aarch64-xilinx-linux --without-python --prefix=/home/ming/Desktop/libxml2/libxml2-2.14.4-aarch64.pkg

make
make install
