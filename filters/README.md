This directory contains the sources of the  C++ effect module
It's based on freeverb of by Jezar at Dreampoint, but other CPU intensive filters can be combined in here to reduce the Python - C++ overhead.

It needs compilation to an .so module before usage, so make sure before first usage:
 - the / partition is opened R/W ("mount -o remount,rw /"
 - the date is set correctly ("date mmddhhmmyy"), TZ=0 =GMT
 - the compilation finished without errors.

To compile perform next command from command line:

g++ -Wall -Wextra -O -ansi -pedantic -fpermissive -shared interface.cpp -o interface.so
