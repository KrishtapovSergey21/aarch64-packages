tar xvf gnuradio-3.10.12.0.tar.gz
cd gnuradio-3.10.12.0
############ update CMakeLists.txt  ###################
comment line 74 and 76 and set this at line 75

set(BOOST_ROOT /home/ming/Desktop/built_packages/boost-1.86.0-aarch64.pkg/usr)

but you need to change path as yours for this "/home/ming/Desktop/built_packages/boost-1.86.0-aarch64.pkg/usr"
#######################################3333333

############ update CMakeLists.txt of gnuradio-runtime  ###################
Add this line after line 30, so this line will be line31
set(BOOST_ROOT /home/ming/Desktop/built_packages/boost-1.86.0-aarch64.pkg/usr)
###########################################

############ update GrBoost.cmake of cmake/Modules  ###################
Add this line after line 18, so this lines will be line19, 20
set(BOOST_ROOT /home/ming/Desktop/built_packages/boost-1.86.0-aarch64.pkg/usr)
set(BOOST_LIBRARYDIR /home/ming/Desktop/built_packages/boost-1.86.0-aarch64.pkg/usr/lib)
###########################################


mkdir build
cmake /home/ming/Desktop/gnuradio-3.10.12.0/gnuradio-3.10.12.0 -DCMAKE_BUILD_TYPE=Release \
  -DPYTHON_EXECUTABLE=/opt/petalinux/2020.1/sysroots/x86_64-petalinux-linux/usr/bin/python3 \
  -DCMAKE_INSTALL_PREFIX=/home/ming/Desktop/gnuradio-3.10.12.0/gnuradio-3.10.12.0-aarch64.pkg \
  -DCMAKE_TOOLCHAIN_FILE=/opt/petalinux/2020.1/sysroots/x86_64-petalinux-linux/usr/share/cmake/OEToolchainConfig.cmake \
  -DBoost_DEBUG=ON \
  -DBOOST_INCLUDEDIR=/home/ming/Desktop/built_packages/boost-1.86.0-aarch64.pkg/usr/include \
  -DBOOST_LIBRARYDIR=/home/ming/Desktop/built_packages/boost-1.86.0-aarch64.pkg/usr/lib \
  -DBoost_NO_BOOST_CMAKE=ON \
  -B /home/ming/Desktop/gnuradio-3.10.12.0/gnuradio-3.10.12.0/build
 
 cd build
 
sudo tar xvf spdlog-1.15.3-aarch64.pkg.tar.xz -C /opt/petalinux/2020.1/sysroots/aarch64-xilinx-linux/
sudo tar xvf fmt-11.2.0.-aarch64.pkg.tar.xz -C /opt/petalinux/2020.1/sysroots/aarch64-xilinx-linux/
sudo tar xvf boost-1.86.0-aarch64.pkg.tar.xz -C /opt/petalinux/2020.1/sysroots/aarch64-xilinx-linux/
sudo tar xvf gsl-2.7-aarch64.pkg.tar.xz  -C /opt/petalinux/2020.1/sysroots/aarch64-xilinx-linux/


make
 
