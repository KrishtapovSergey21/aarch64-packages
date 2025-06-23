git clone --branch v28.0 --depth 1 https://github.com/protocolbuffers/protobuf.git
cd protobuf
git submodule update --init --recursive

cmake -DCMAKE_SYSTEM_NAME=Linux \
>   -DCMAKE_SYSTEM_PROCESSOR=aarch64 \
>   -DCMAKE_INSTALL_PREFIX=/home/ming/Desktop/bond/usr \
>   -Dprotobuf_BUILD_TESTS=OFF

make PREFIX=/home/ming/Desktop/bond/usr

sudo make install PREFIX=/home/ming/Desktop/bond/usr