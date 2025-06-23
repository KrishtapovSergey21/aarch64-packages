When default cmake configuration is failed.
Error : 
CMake Error at CMakeLists.txt:37 (message):
  In-source builds in /home/ming/Desktop/itplayer/codec2/codec2-1.2.0 are not
  allowed, please remove ./CMakeCache.txt and ./CMakeFiles/, create a
  separate build directory and run cmake from there.

- And after configuration, some math functions are missed. so CMakeList.txt has to update.
	Add that line at #28
		set(CMAKE_REQUIRED_LIBRARIES m)

- how to fix
cd /home/ming/Desktop/itplayer/codec2/codec2-1.2.0
rm -rf CMakeCache.txt CMakeFiles/
mkdir build
cd build
cmake -DCMAKE_BUILD_TYPE=Release \
	-DCMAKE_INSTALL_PREFIX=/home/ming/Desktop/itplayer/codec2-1.2.0-aarch84.pkg \
	-DCMAKE_SYSTEM_PROCESSOR=aarch64 \
	-DBUILD_SHARED_LIBS=ON \
	-DBUILD_STATIC_LIBS=OFF \
	-DCMAKE_SYSTEM_NAME=Linux..

make install
