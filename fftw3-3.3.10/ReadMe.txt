tar xvf fftw3-3.3.10.tar.xz
cd fftw3-3.3.10

cmake -DCMAKE_SYSTEM_NAME=Linux -DCMAKE_SYSTEM_PROCESSOR=aarch64 -DBUILD_SHARED_LIBS=ON -DBUILD_STATIC_LIBS=OFF -DENABLE_FLOAT=ON -DENABLE_THREADS=ON   -DCMAKE_INSTALL_PREFIX=/home/ming/Desktop/gnss/project/work/fftw-3.3.10-aarch64.pkg ..   --disable-static   --enable-threads   -enable-maintainer-mode  --disable-doc
sudo make
sudo make install