

# $ g++ -std=c++11 -c main.cpp -I/usr/local/include
# $ g++ main.o -o main -I/usr/local/include -L/usr/local/lib -lgrt
# $ ./main

CC=g++

CPPFILE=*

SOURCES=$(CPPFILE).cpp

INCLUDE_PATH= -I /usr/local/include
LIB_PATH= -L /usr/local/lib
LIB_FLAGS= -lgrt


EXECUTABLE = main
OBJECTS= $(SOURCES:.cpp=.o)


%.o: %.cpp
	$(CC) -std=c++11 -c $< $(INCLUDE_PATH)

all: $(OBJECTS)
	$(CC) $(OBJECTS) -o $(EXECUTABLE) $(INCLUDE_PATH) $(LIB_PATH) $(LIB_FLAGS)

run:
	./$(EXECUTABLE)

clean:
	rm -f *.o *~ $(EXECUTABLE)
