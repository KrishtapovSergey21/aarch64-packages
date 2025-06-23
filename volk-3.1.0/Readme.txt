tar xvf volk-3.1.0.tar.gz
cd volk-3.1.0/
cd /home/ming/Desktop/itplayer/libvolk/volk-3.1.0
mkdir build
cd build
cmake -DCMAKE_SYSTEM_NAME=Linux \
      -DCMAKE_SYSTEM_PROCESSOR=aarch64 \
      -DCMAKE_INSTALL_PREFIX="/home/ming/Desktop/itplayer/volk-3.1.0-aarch64.pkg/usr" \
      -DBUILD_SHARED_LIBS=ON \
      -DBUILD_STATIC_LIBS=OFF \
      -DBUILD_gflags_nothreads_LIB=OFF \
      ..
make
make install

--------------------------------------------------------------------------------------------
Error : 

-- Python checking for mako >= 0.4.2
-- Python checking for mako >= 0.4.2 - not found
CMake Error at CMakeLists.txt:167 (message):
  Mako templates required to build VOLK


-- Configuring incomplete, errors occurred!
See also "/home/ming/Desktop/itplayer/libvolk/volk-3.1.0/build/CMakeFiles/CMakeOutput.log".

--------------------------------------------------------------------------------------------
- install python mako and reconfiguration
	sudo /opt/petalinux/2020.1/sysroots/x86_64-petalinux-linux/usr/bin/python3 -m ensurepip --upgrade
	/opt/petalinux/2020.1/sysroots/x86_64-petalinux-linux/usr/bin/python3 -m pip install --user mako

	rm -rf *
	cmake -DCMAKE_SYSTEM_NAME=Linux \
      		-DPYTHON_EXECUTABLE=/usr/bin/python3 \
      	-DCMAKE_SYSTEM_PROCESSOR=aarch64 \
      	-DCMAKE_INSTALL_PREFIX="/home/ming/Desktop/itplayer/volk-3.1.0-aarch64.pkg/usr" \
      	-DBUILD_SHARED_LIBS=ON \
      	-DBUILD_STATIC_LIBS=OFF \
      	-DBUILD_gflags_nothreads_LIB=OFF \
      	..


	sudo make install

