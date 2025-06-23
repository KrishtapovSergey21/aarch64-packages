// Armadillo
wget https://sourceforge.net/projects/arma/files/armadillo-14.4.1.tar.xz

tar xvfz armadillo-14.4.1.tar.xz
cd armadillo-14.4.1
cmake -DCMAKE_SYSTEM_NAME=Linux -DCMAKE_SYSTEM_PROCESSOR=aarch64 -DBUILD_SMOKE_TEST=OFF -DCMAKE_INSTALL_PREFIX=/home/ming/Desktop/gnss/project/work/armadillo-14.4.1-aarch64.pkg ..
make
make install