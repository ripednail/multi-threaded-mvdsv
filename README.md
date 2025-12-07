This is a compile of the mvdsv source with LLVM/cmake with OPEN CILK 3.0

I believe multi threaded quake servers are most applicable to low power systems with multiple cpus (raspberry pi nano 2w or similar). There are also some idle cpu improvements in mvdsv and ktx.

It would be great if someone would go through the code and convert it from cilk to omp so that is more compatible with the latest mvdsv/ktx builds.

You can download the opencilk binaries here: https://github.com/OpenCilk/opencilk-project/releases
Just extract to a directory and export the compiler to compile or run mvdsv

Example termianl command: export PATH=/home/vboxuser/Downloads/opencilk-3.0.0-x86_64-linux-gnu-ubuntu-24.04/bin/:$PATH

I have included the updated make file for SMPMVDSV as well to compile

So you'll just need to download the source if you want to compile or just run the binary and set the number of threads


export CILK_NWORKERS=4
./smpmvdsv



if your using the ktx mod make sure you download the 32 bit version 

Additonally I downloaded the latest KTX mod and configured the compile script to use cmake with 32 bit flags.

Use the following to compile ./build_cmake.sh linux-i686
