# wasm-openssl

emconfigure ./Configure gcc -no-tests -no-asm -static -no-sock
sed -i 's|^CROSS_COMPILE.*$|CROSS_COMPILE=|g' Makefile
emmake make -j 1 build_generated libssl.a libcrypto.a
