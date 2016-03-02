apt-get install build-essential automake libtool git

git clone https://github.com/Long-live-shadowsocks/ShadowVPN.git

git submodule update --init

./autogen.sh

./configure --enable-static --sysconfdir=/etc

make 

make install

vi /etc/shadowvpn/server.conf
