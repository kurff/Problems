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

Problem: GLIBC_2.14 not found

Solution: gcc -static


Problem: undefined reference to `TLS init function for caffe2::CUDAContext::cuda_objects_'

Solution: update gcc (in my case, update gcc-4.8.2 -> gcc-4.8.3)


Problem: update gcc on CentOS

Solution: unset LIBRARY_PATH CPATH C_INCLUDE_PATH PKG_CONFIG_PATH CPLUS_INCLUDE_PATH INCLUDE


Problem: checking for suffix of object files... configure: error: in `/home/manu/gcc/gcc/i686-pc-linux-gnu/libgcc':
         configure: error: cannot compute suffix of object files: cannot compile

Solution: Required libraries for the GCC build are missing, specifically MPFR, GMP and MPC. If installed as shared libraries they must be in the runtime linker's search path so they can be found. 


Problem: loss can not reduce in training neural networks

Solution: initialization is very important


Problem: Nginx [emerg]: bind() to 0.0.0.0:80 failed (98: Address already in use)


Solution: sudo fuser -k 80/tcp


Problem: install Fcgi 'EOF' was not declared in this scope
Solution: 在./include/fcgio.h文件中加上 #include <cstdio>
