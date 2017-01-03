# Problems

https://www.centos.org/forums/viewtopic.php?t=58548#p247228

Problem:   OpenCV not finding libavcodec installed in centos

solution:  export PKG_CONFIG_PATH=/usr/local/lib/pkgconfig

Problem:   OpenCV make fails - “recompile with -fPIC”

Solution:  ./configure --disable-shared -with-pic

Problem:   /lib/libbz2.so.1: could not read symbols: File in wrong format  build Opencv

Solution:  sed -i 's#/lib/libbz2.so.1#/lib64/libbz2.so.1#g' CMakeCache.txt

Problem:  stdc++ can not find

Solution: sudo yum install libstdc++-static
