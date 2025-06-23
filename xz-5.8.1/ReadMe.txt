sudo dpkg -i gettext_0.19.8.1-10build1_amd64.deb
sudo dpkg -i po4a_0.57-2_all.deb

tar xvf xz-5.8.1.tar.gz
cd xz-5.8.1

./configure --host=aarch64-xilinx-linux --prefix=/home/ming/Desktop/xz-5.8.1/xz-5.8.1-aarch64.pkg

make
make install

