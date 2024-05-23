CPP      = g++
OBJ      = main.o
LIBS     = -m32 -lopengl32 -lglu32 -lfreeglut
BIN      = Fort_Zeelandia

# Check the OS and set the RM and executable accordingly
ifeq ($(OS),Windows_NT)
    RM = del /Q
    EXE = $(BIN).exe
else
    RM = rm -f
    EXE = $(BIN)
endif

.PHONY: all clean run

all: $(EXE)

clean:
	$(RM) $(OBJ) $(EXE)

$(EXE): $(OBJ)
	$(CPP) $(OBJ) -o $(EXE) $(LIBS)

main.o: main.cpp
	$(CPP) -c main.cpp -o main.o -std=c++11 -m32

run: all
	$(EXE)
