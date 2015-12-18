# Installation

First, to install the newest version of [NTL]. You can use the [GMP] library as the long integer library. To do so, you should use `./configure NTL_GMP_LIP=on` to set up the configuration. Since the 7.0 ver., [NTL] supports thread-safe routines. To use `NTL_THREADS=on` to switch it on. 
P.S., by using the multithreads feature, you should also add `-lpthread` to the linking flags. 

[NTL]: http://www.shoup.net/ntl/download.html
[GMP]: https://gmplib.org