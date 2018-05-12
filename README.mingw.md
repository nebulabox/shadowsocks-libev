Build on MinGW w64
=======

Install msys2 https://msys2.github.io/

Launch the “MinGW-w64 Win32 Shell” from the Start Menu.

Install 32-bit toolchain
```bash
pacman -S mingw-w64-i686-toolchain git cmake diffutils tar perl make openssl asciidoc xmlto mingw-w64-i686-mbedtls mingw-w64-i686-c-ares mingw-w64-i686-libsodium mingw-w64-i686-pcre
```

Build libev
```bash
git clone https://github.com/nebulabox/libev.git
cd libev
./configure
make && make install
```

Build shadowsocks-libev
```bash
git clone https://github.com/nebualbox/shadowsocks-libev.git
./configure --enable-static --disable-shared --disable-system-shared-lib --disable-documentation --disable-ssp
make -j2
make install 
```
