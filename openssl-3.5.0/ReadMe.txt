tar xvf openssl-3.5.0.tar.gz
cd openssl-3.5.0

./Configure linux-aarch64 --prefix=/home/ming/Desktop/openssl-3.5.0/openssl-3.5.0-aarch64.pkg

"set CROSS_COMPILE as empty string in line 1681 of Makefile"

make
make install

