cmake -DCMAKE_SYSTEM_NAME=Linux \
	  -DCMAKE_SYSTEM_PROCESSOR=aarch64 \
	  -DCMAKE_INSTALL_PREFIX="/home/ming/Desktop/itplayer/libpcap/usr" \
          -DBUILD_SHARED_LIBS=ON \
	  -DBUILD_STATIC_LIBS=OFF \



make install
