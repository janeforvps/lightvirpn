apt-get update

apt-get install build-essential automake libtool git

git clone https://github.com/Long-live-shadowsocks/ShadowVPN.git

git submodule update --init

./autogen.sh

./configure --enable-static --sysconfdir=/etc

make 

make install

vi /etc/shadowvpn/server.conf

shadowvpn -c /etc/shadowvpn/server.conf -s start

xxd -l 8 -p /dev/random
