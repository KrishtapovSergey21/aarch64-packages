$ libtoolize --force --copy --automake
$ aclocal
$ autoheader
$ automake --foreign --copy --add-missing
$ autoconf
$ ./configure --enable-cxx --host=aarch64-xilinx-linux --prefix=/home/ming/Desktop/alsa-lib/alsa-lib-1.2.14-aarch64.pkg
$ make
$ make install
