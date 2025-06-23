 
Latest release v1.14.6 is failed, earler version(1.13.4, 1.12.3, does not support cross-complie!!
CMake Error at CMakeLists.txt:1 (cmake_minimum_required):
  CMake 3.18 or higher is required.  You are running version 3.15.3
 
So Use Cmake used 3.18.6
	  
https://sgb-apac-29.75b8814ba98de5c51115eceabd5fc23e.r2.cloudflarestorage.com/6FKVE-0YA2I-AIRFK-367BW/hdf5-1.14.6.tar.gz?response-content-disposition=attachment%3B filename%3D%22hdf5-1.14.6.tar.gz%22&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=80d07ac26ce4de7e1edd218b5926e9af%2F20250621%2Fapac%2Fs3%2Faws4_request&X-Amz-Date=20250621T132839Z&X-Amz-SignedHeaders=host&X-Amz-Expires=600&X-Amz-Signature=328ad225626fc971a8704e51f47d65b22a088075249332445fdc65ec1d98f183

cd hdf5-1.14.6
mkdir build
cd build
cmake .. -DCMAKE_SYSTEM_NAME=Linux \
	  -DCMAKE_SYSTEM_PROCESSOR=aarch64 \
	  -DCMAKE_INSTALL_PREFIX=/home/ming/Downloads/hdf5/usr \
	  -DBUILD_SHARED_LIBS=ON \
	  -DBUILD_STATIC_LIBS=OFF \
	  -DCMAKE_CROSSCOMPILING=true \
	  -DBUILD_TESTING=OFF \
	  -DZLIB_ROOT=/opt/petalinux/2020.1/sysroots/aarch64-xilinx-linux/usr
	  
make -j4  
make install



