ATSAMD21 mcu base project.

Prerequisite: arm compiler (arm-none-eabi- )

Works with both c and c++. Automatic folder scanning for .h and .c/.cpp files in src/ and lib/
Add relative path for files you dont want compiled in makefile INGNORE variable ( ex. ./lib/testlib/nocompile.c \ ) note the backslash
Also change the linker script for the mcu you're using. Linker scripts are in ./init/linker_script and makefile variable is LINKER_SCRIPT
Use ./init/svd/ files for easier debugging if your debugger supports it.
Change ./lib/samd21x with another one from ./samd21bcd depending on the mcu version your're using and then change the defines for your mcu in the makefile and in ./.vscode/c_cpp_properties.json

usage 
make         -to build
make clean   -to delete all buildfiles