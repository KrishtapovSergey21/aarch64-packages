sudo apt install gcc-aarch64-linux-gnu

make lib/libgsm.a CC=aarch64-linux-gnu-gcc CFLAGS="-fPIC -Iinc -O2 -Wall -c"

INSTALL_ROOT="/home/ming/Desktop/bond/usr"

aarch64-linux-gnu-gcc -shared -Wl,-soname,libgsm.so.1 -o "${INSTALL_ROOT}/lib/libgsm.so.1.0.22" src/*.o

mkdir -p "${INSTALL_ROOT}/include/gsm"

aarch64-linux-gnu-gcc -shared -Wl,-soname,libgsm.so.1 -o "${INSTALL_ROOT}/lib/libgsm.so.1.0.22" src/*.o

(cd "${INSTALL_ROOT}/lib" && ln -sf libgsm.so.1.0.22 libgsm.so.1)

(cd "${INSTALL_ROOT}/lib" && ln -sf libgsm.so.1 libgsm.so)

install -m 644 inc/gsm.h "${INSTALL_ROOT}/include/gsm/"

