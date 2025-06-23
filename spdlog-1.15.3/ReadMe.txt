tar xvf spdlog-1.15.3.tar.xz
cd spdlog-1.15.3
cmake ../spdlog \
  -DCMAKE_SYSTEM_NAME=Linux \
  -DCMAKE_SYSTEM_PROCESSOR=aarch64 \
  -DCMAKE_INSTALL_PREFIX=/home/ming/Desktop/Work/spdlog-1.15.3-aarch64.pkg/usr \
  -DBUILD_SHARED_LIBS=ON \
  -DBUILD_STATIC_LIBS=OFF \
  -DBUILD_gflags_nothreads_LIB=OFF
sudo make
sudo make install