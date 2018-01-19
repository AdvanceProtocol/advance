Advance Protocol staging tree 0.13.0
===============================

https://advanceprotocol.net


What is Advance?
----------------

Advance is an experimental new digital currency that enables anonymous, instant
payments to anyone, anywhere in the world. Advance uses peer-to-peer technology
to operate with no central authority: managing transactions and issuing money
are carried out collectively by the network. Advance Protocol is the name of the open
source software which enables the use of this currency.

For more information, as well as an immediately useable, binary version of
the Advance Protocol software, see https://advanceprotocol.net.


License
-------

Advance Protocol is released under the terms of the MIT license. See [COPYING](COPYING) for more
information or see https://opensource.org/licenses/MIT.


Compile from source
-------------------
**Requirements**
```
Windows only: apt-get install g++-mingw-w64-x86-64 g++-mingw-w64-i686 mingw-w64-i686-dev

apt-get install libqt5gui5 libqt5core5a libqt5dbus5 qttools5-dev qttools5-dev-tools libprotobuf-dev protobuf-compiler
apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils libminiupnpc-dev
apt-get install libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev
add-apt-repository ppa:bitcoin/bitcoin
apt-get update
apt-get install libdb4.8-dev libdb4.8++-dev
apt-get install automake autotools-dev git curl
```

**Linux x64 (static)**
```
git clone https://github.com/AdvanceProtocol/advance advance-linux
cd advance-linux
cd depends
make
cd ..
./autogen.sh
./configure --enable-glibc-back-compat --prefix=`pwd`/depends/x86_64-pc-linux-gnu LDFLAGS="-static-libstdc++"
make
```

**Windows (x64) (static)**
```
git clone https://github.com/AdvanceProtocol/advance advance-win64
cd advance-win64
cd depends
make HOST=x86_64-w64-mingw32 
cd ..
./autogen.sh
CONFIG_SITE=$PWD/depends/x86_64-w64-mingw32/share/config.site ./configure --prefix=/
make
```

**Windows (x86) (static)**
```
git clone https://github.com/AdvanceProtocol/advance advance-win32
cd advance-win32
cd depends
make HOST=i686-w64-mingw32
cd ..
./autogen.sh
CONFIG_SITE=$PWD/depends/x86_64-w64-mingw32/share/config.site ./configure --prefix=/
make
```
