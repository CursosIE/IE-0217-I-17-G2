#Autor: David Corrales Retana

IDIR =../include
INCLUDES=-I$(IDIR)
CFLAGS =-Wall
CC=g++

ODIR=../build

_DEPS = functions.hpp
DEPS = $(patsubst %,$(IDIR)/%,$(_DEPS))

_OBJ = functions.o main.o
OBJ = $(patsubst %,$(ODIR)/%,$(_OBJ))

$(ODIR)/%.o: %.cpp $(DEPS)
	$(CC) $(CFLAGS) -c -o $@ $< $(INCLUDES)

EXE=matrix

$(ODIR)/$(EXE): $(OBJ)
	$(CC) $(CFLAGS) -o $@ $^ $(INCLUDES)


.PHONY: clean


gdb:
	gdb $(ODIR)/$(EXE)

run:
	$(ODIR)/$(EXE)

clean:
	rm -f $(ODIR)/*.o $(ODIR)/*~ $(ODIR)/$(EXE) $(ODIR)/*.txt
