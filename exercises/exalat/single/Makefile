# 
# Makefile for cuda-intro
#

MF= Makefile

EXE= exercise.exe
SRC= exercise.cu

ARCH=sm_35

CC=	nvcc
CFLAGS+=-O3 -arch=$(ARCH)

default: $(EXE)


.SUFFIXES:
.SUFFIXES: .cu  .o

OBJ=	$(SRC:.cu=.o)

.cu.o:
	$(CC) $(CFLAGS) -dc -c $<

$(EXE):	$(OBJ) 
	$(CC) $(CFLAGS) -o $@ $(OBJ) 

$(OBJ):	$(MF) 

clean:
	rm -f $(OBJ) $(EXE) core slurm*.out slurm*.err
