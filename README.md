# file_compilation
A group of folders that gives an example on how to compile c++ files with dependent files located in different directories.

This repository holds a folder that contains two copies of 'my_file.cpp', which contains two functions that are declared in cpp files contained in the 'folder' folder.
There is one copy of my_file.cpp in the main directory of the folder, and another copy of it in the 'program' folder. Each of these have a Makefile alongside it that can be run to compile the program.

This repository serves as an example on how to compile a program that depends on multiple files that are located in different directories. The makefiles are commented, and include both what the final output should be if unchanged, including a more modular portion (used in the compilation) that can be modified for your own programs.
