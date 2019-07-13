# pi-cpuminer-linux-


sudo apt-get update

sudo apt-get install automake autoconf pkg-config libcurl4-openssl-dev libjansson-dev libssl-dev libgmp-dev make g++

sudo apt-get install wget git-core

mkdir miner

cd miner

git clone https://github.com/tpruvot/cpuminer-multi.git

cd cpuminer-multi/

./autogen.sh

./build.sh

./autogen.sh && CFLAGS="-march=native" ./configure --disable-aes-ni && make

./cpuminer -a scrypt -o stratum+tcp://us.litecoinpool.org:3333 -u Holiday.rpi -p x
