// Gflags
tar xvf gflags-v2.2.2.tar.gz
cd gflags-2.2.2/
cmake -DCMAKE_SYSTEM_NAME=Linux -DCMAKE_SYSTEM_PROCESSOR=aarch64 -DBUILD_SHARED_LIBS=ON -DBUILD_STATIC_LIBS=OFF -DBUILD_gflags_nothreads_LIB=OFF -DCMAKE_INSTALL_PREFIX=/home/ming/Desktop/gnss/project/work/gflags-2.2.2-aarch64.pkg ..
make
make install