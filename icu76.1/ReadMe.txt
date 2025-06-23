tar xvf icu_76.1.orig.tar.gz
cd icu/source
mkdir ../host-build
cd ../host-build
# this should be run with x86_64 without source petalinux

/home/ming/Desktop/icu76.1/icu/source/runConfigureICU Linux
make -j$(nproc)
cd ../source

# set source as petalinux again

source /opt/petalinux/2020.1/environment-setup-aarch64-xilinx-linux
./configure \
  --host=aarch64-xilinx-linux \
  --prefix=/home/ming/Desktop/icu76.1/icu76.1-aarch64.pkg \
  --disable-samples \
  --disable-tests \
  --with-cross-build=/home/ming/Desktop/icu76.1/icu/host-build

make
make install
