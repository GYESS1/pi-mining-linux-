# pi-cpuminer-linux-


sudo apt-get update

sudo apt-get install automake autoconf pkg-config libcurl4-openssl-dev libjansson-dev libssl-dev libgmp-dev make g++

sudo apt-get install wget git-core

mkdir miner

cd miner

git clone https://github.com/GYESS1/cpuminer-multi.git

cd cpuminer-multi/

./autogen.sh

./build.sh

./autogen.sh && CFLAGS="-march=native" ./configure --disable-aes-ni && make

./cpuminer -a scrypt:1048576 -o stratum+tcp://vrmpool.raspi-ninja.com:3332 -u jam1.pi1 -p x
