

# make the subdir first
CXX = g++
#FLAG = -O3 -static 
FLAG = -O3
SHELL :=/bin/bash

ComplexToolDir = ./Complex_Tool_src
ComplexToolEXE = /Complex_Tool

all: Complex_Tool PDB_To_SEQ_miss MAT_To_Column DistMat_To_ContMat

Complex_Tool:
	cd $(ComplexToolDir)&&make
	mv ${ComplexToolDir}$(ComplexToolEXE) ../

PDB_To_SEQ_miss:
	${CXX} PDB_To_SEQ_miss.cpp ${FLAG} -o PDB_To_SEQ_miss
	mv PDB_To_SEQ_miss ../util

MAT_To_Column:
	${CXX} MAT_To_Column.cpp ${FLAG} -o MAT_To_Column
	mv MAT_To_Column ../util

DistMat_To_ContMat:
	${CXX} DistMat_To_ContMat.cpp ${FLAG} -o DistMat_To_ContMat
	mv DistMat_To_ContMat ../util


# clean all the temp files
clean:
