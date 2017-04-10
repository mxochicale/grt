# Usage

[linuxosx-linking-instructions](https://github.com/nickgillian/grt/tree/master/build#linuxosx-linking-instructions)

main.cpp
---

```
#include<iostream>
using namespace std;

#include <GRT/GRT.h>
using namespace GRT;

int main (int argc, const char * argv[])
{
    //Print the GRT version
    cout << "GRT Version: " << GRTBase::getGRTVersion() << endl;

    return EXIT_SUCCESS;
}
```



# Compiling in the terminal
```
   $ g++ -std=c++11 -c main.cpp -I/usr/local/include  
   $ g++ main.o -o main -I/usr/local/include -L/usr/local/lib -lgrt  
   $ ./main
```

#### Errors
```
$ ./main  
./main: error while loading shared libraries: libgrt.so: cannot open shared object file: No such file or directory
```


Solution
```
$ find ~/ -type f -name "libgrt.so"   
  /home/map479-admin/github/grt/build/tmp/libgrt.so
```
add the following line to the .bashrc
```
LD_LIBRARY_PATH=/home/map479-admin/github/grt/build/tmp/:$LD_LIBRARY_PATH
```
[Reference](https://www.cs.swarthmore.edu/~newhall/unixhelp/howto_C_libraries.html)


Output
---

```
$ g++ -std=c++11 -c main.cpp -I/usr/local/include  
$ g++ main.o -o main -I/usr/local/include -L/usr/local/lib -lgrt  
$ ./main

GRT Version: 0.1.0 revision: 20-Feb-2016

```

#### Using Makefile


Create link file
```
CC=g++

CFLAGS=-Wall


INCLUDE_PATH= -I /usr/local/include
LIB_PATH= -L /usr/local/lib
LIB_FLAGS= -lgrt


EXECUTABLE = main
SOURCES=main.cpp
OBJECTS= $(SOURCES:.cpp=.o)


%.o: %.cpp
	$(CC) -std=c++11 -c $< $(INCLUDE_PATH)

all: $(OBJECTS)
	$(CC) $(OBJECTS) -o $(EXECUTABLE) $(INCLUDE_PATH) $(LIB_PATH) $(LIB_FLAGS)

clean:
	rm -f *.o *~ $(EXECUTABLE)
```


## Build the project
```
make
```


## Clean the project
```
make clean
```











# Machine GTR Tested on


```
$ uname -a
Linux eee320 3.13.0-92-generic #139-Ubuntu
SMP Tue Jun 28 20:42:26 UTC 2016 x86_64 x86_64 x86_64 GNU/Linux
```

```
$ lsb_release -a
No LSB modules are available.
Distributor ID:	Ubuntu
Description:	Ubuntu 14.04.3 LTS
Release:	14.04
Codename:	trusty
```
