$ cd <uhd-repo-path>/host
$ mkdir build
$ cd build
$ cmake -DCMAKE_SYSTEM_NAME=Linux -DCMAKE_SYSTEM_PROCESSOR=aarch64 -DPYTHON_EXECUTABLE=$(which python3) -DCMAKE_INSTALL_PREFIX=/home/ming/Desktop/libuhd-4.8.0.0-aarch64.pkg ../
$ make 
$ make install
