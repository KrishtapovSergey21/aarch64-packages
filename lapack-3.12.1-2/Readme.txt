1. Install Fortran Compiler

$ tar -xvf gfortran-aarch64-linux-gnu.tar.xz
$ cd gfortran-aarch64-linux-gnu
$ sudo dpkg -i *.deb


2. Install lapack

$ tar -xvf lapack-3.12.1.tar.gz
$ cd lapack-3.12.1
$ mkdir build
$ cd build
$ cmake -DCMAKE_SYSTEM_NAME=Linux -DCMAKE_SYSTEM_PROCESSOR=aarch64 -DCMAKE_Fortran_COMPILER=/usr/bin/aarch64-linux-gnu-gfortran -DCMAKE_INSTALL_PREFIX=/home/ming/Desktop/lapack-3.12.1-aarch64.pkg ..
$ cmake --build . -j --target install