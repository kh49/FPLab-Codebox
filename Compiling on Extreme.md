for cmake - need to specify local compilation/installation - 

sourcing unknown libraries: https://www.cfd-online.com/Forums/openfoam-installation/118558-how-solve-zlib-h-missing-problem-without-root-right.html

checking if library error is due to ld or cmake with ld -l[name of library] --verbose, then directing cmake: https://github.com/mreppell/Karp/issues/2

-DCMAKE_PREFIX_PATH=/usr/lib/x86_64-linux-gnu/


final cmake -with required  cmake libraries in lib64: 

cmake -DBOOST_ROOT=/export/share/apps/boost-1.65.0 -DCMAKE_C_COMPILER=/export/share/compilers/gcc-7.2.0/bin/gcc -DCMAKE_INSTALL_PREFIX=/export/home/khuang49/bin/[desired install directory] -DCMAKE_PREFIX_PATH=/lib64/ ..

for build breaking warnings that aren't actually errors: http://forums.codeblocks.org/index.php?topic=19202.0
https://stackoverflow.com/questions/7543978/how-to-pass-g3-flag-to-gcc-via-make-command-line

export CFLAGS="-W no-deprecated-declarations"
