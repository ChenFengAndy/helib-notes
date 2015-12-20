# Installation

Firstly, we need to install the newest version of [NTL]. We can download the source code from Victor's [home page](http://www.shoup.net/ntl/download.html) or download my forked version in [github](git@github.com:fionser/NTL.git). By installing the NTL, we should go into the `src` directory and just call `./configure` and call the `make` command. After waiting for several minutes, we should call the `sudo make install` command. This command copies the necessary header files and objects files into your building path. 

According to Victor's description, we can use the [GMP] library as the alternative library for multiple precision. The GMP library gives a better performance, but I have no ran any benchmarks on it yet. To use the [GMP], we should firstly install the [GMP] from its official page. Then, we should use `./configure NTL_GMP_LIP=on` when we are going to configure the NTL. When we are compiling our source codes, we need to add extra flag `-lgmp` to tell the linker for using the [GMP] library. 

Besides, if the path of GMP we have installed is not the _normal_ path (the `/usr/include` or `/usr/local/include`), we need to add `GMP_PREFIX=XXXX` to the `./configure` command. We also need to tell compiler and linker about the path of the installed GMP. For example, by adding flags `-I path_to_header_files -L path_to_object_files`, where the path follows `-I` is the path of GMP header files the path follows `-L` is the path of GMP object files. 

Since the 7.0 version, [NTL] supports thread-safe routines. By adding `NTL_THREADS=on` to the `./configure` command to build the NTL with mult-threads feature. Besides, we should also add `-lpthread` to tell the linker to use the multi-threads library. 
However, current multi-threads of [HElib] only works for Ubuntu with compiler version not lower than g++4.9. 

Finally, we can install the [HElib] by now. Firstly download it from the github. The installation of [HElib] is similar to the installation of [NTL]: go into the `src` directory; call the `./configure` command then the `make` and `make install` commands. To use multi-threads feature, we add flag `-DFHE_THREADS` to the `./configure` command. 

[NTL]: http://www.shoup.net/ntl/download.html
[GMP]: https://gmplib.org
[HElib]: https://github.com/shaih/HElib