## Crypto Block Explorers (version 3):
1. https://explorer.crypt-o-coin.cash
2. https://explorer.test.crypt-o-coin.cash/

## **Compiling Crypto daemon on Ubuntu 18.04**

``sudo apt update``

``sudo apt install git build-essential cmake libboost-all-dev miniupnpc libunbound-dev graphviz doxygen libunwind8-dev pkg-config libssl-dev libcurl4-openssl-dev libgtest-dev libreadline-dev libzmq3-dev libsodium-dev libhidapi-dev libhidapi-libusb0``

``cd ~``

``git clone --recursive https://github.com/GonzoTheDev/crypto.git``

``cd crypto``

``USE_SINGLE_BUILDDIR=1 make -j<number of threads>``

The binaries compiled at ``~/crypto/build/release/bin/``

Run and sync the Daemon with ``./cryptocoind``

***

## Compile and run the cryptoblocks

    cd ~
    git clone https://github.com/GonzoTheDev/cryptocoin-blockchain-explorer.git cryptoblock
    cd cryptoblock
    mkdir build && cd build
    cmake ..
    make -j<number of threads>
    
    # run the explorer:
    ./cryptoblocks -x 127.0.0.1 --testnet-url https://explorer.test.crypt-o-coin.cash --enable-emission-monitor --enable-autorefresh 
    
    optional --enable-json-api --enable-pusher
    

Open explorer with your browser:
http://127.0.0.1:8081


[README_original.md](README_original.md)
