# Problems

https://www.centos.org/forums/viewtopic.php?t=58548#p247228

Problem:   OpenCV not finding libavcodec installed in centos

solution:  export PKG_CONFIG_PATH=/usr/local/lib/pkgconfig

Problem:   OpenCV make fails - “recompile with -fPIC”

Solution:  ./configure --disable-shared -with-pic
