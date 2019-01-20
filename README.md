# install
## log4cpp

First, get the installation package of log4app.
------------------------------------------------
$ wget https://sourceforge.net/projects/log4cpp/files/log4cpp-1.1.x%20%28new%29/log4cpp-1.1/log4cpp-1.1.3.tar.gz
------------------------------------------------

Second, decompress.
------------------------------------------------
$ tar -zxvf log4cpp-1.1.3.tar.gz
------------------------------------------------

Finally, auto install
------------------------------------------------
$ ./configure
$ make
$ make check
$ make install
------------------------------------------------
This will install log4cpp under /usr/local.
