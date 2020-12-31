# SUPPOSE THAT WE HAVE A FOLDER LOCATED AT:
# /home/kyleperez/zztest
# WITH A folder 'folder' and two files my_file.cpp and makefile
#		folder contains fhw.cpp and fhw.h and a folder 'other_one'
#			other_one contains other.cpp and other.h
# THE zztest FOLDER CONTAINS THE FILES THAT my_file.cpp NEEDS IN ORDER TO COMPILE
# TO COMPILE THE PROGRAM, USE THE FOLLOWING MAKEFILE:
#
#
#OUTPUT OF THE MAKEFILE:
#my_file : my_file.cpp \
#	folder/fhw.cpp \
#	folder/other_one/other.cpp
#	g++ \
#	-I folder \
#	-I folder/other_one \
#	-o my_file \
#	my_file.cpp \
#	folder/fhw.cpp \
#	folder/other_one/other.cpp
#
#RUNS: g++ -I folder -I folder/other_one -o my_file my_file.cpp folder/fhw.cpp folder/other_one/other.cpp

# Name of the executable
EXECUTABLE = my_file
# Name of the cpp file the executable is based on
EXECUTABLE_FILE = $(EXECUTABLE).cpp

# Name of the dependent file
DEPENDENT_FILE_1 = fhw.cpp
# Directory we find the file in
#	'..' implies we go up by one directory from where the Makefile is located
DIRECTORY_FILE_1 = folder
# Location of the file (including its name)
LOCATION_FILE_1 = $(DIRECTORY_FILE_1)/$(DEPENDENT_FILE_1)

# Same as above, for another file
DEPENDENT_FILE_2 = other.cpp
DIRECTORY_FILE_2 = folder/other_one
LOCATION_FILE_2 = $(DIRECTORY_FILE_2)/$(DEPENDENT_FILE_2)

# We include the directories in which the dependent files are located
INCLUDED_PATHS = -I $(DIRECTORY_FILE_1) \
	-I $(DIRECTORY_FILE_2)
	
# All the files needed to produce the executable
INCLUDED_FILES = $(EXECUTABLE_FILE) \
	$(LOCATION_FILE_1) \
	$(LOCATION_FILE_2)

# What the executable depends on
$(EXECUTABLE) : $(INCLUDED_FILES)
	# The terminal command run to produce the executable
	g++ \
	$(INCLUDED_PATHS) \
	-o $(EXECUTABLE) \
	$(INCLUDED_FILES)
		
# Enter 'make clean' to remove the executable	
	
clean :
	rm my_file
	
