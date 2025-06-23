tar xvf elfutils-0.193.tar.bz2
cd elfutils-0.193

./configure --host=aarch64-xilinx-linux --prefix=/home/ming/Desktop/libelf-0.193/elfutils-0.193-aarch64.pkg

make
make install

