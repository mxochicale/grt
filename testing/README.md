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




# Some Compilation Errors


```
~/examples/UtilExamples/ThreadPoolExample$ ./main
Error, this example can only be run if the
GRT is built with C++11 support!
```


```

~/examples/tests/DataStructures/*.cpp$ make


~/examples/tests/Util$ make
g++ -std=c++11 -c TypedefsTest.cpp -I /usr/local/include/GRT
g++ *.o -o main -I /usr/local/include/GRT -L /usr/local/lib -lgrt
TypedefsTest.o: In function `Typedefs_Sqr_Test::TestBody()':
TypedefsTest.cpp:(.text+0x120): undefined reference to `testing::internal::AssertHelper::AssertHelper(testing::TestPartResult::Type, char const*, int, char const*)'
TypedefsTest.cpp:(.text+0x136): undefined reference to `testing::internal::AssertHelper::operator=(testing::Message const&) const'
TypedefsTest.cpp:(.text+0x145): undefined reference to `testing::internal::AssertHelper::~AssertHelper()'
.
.
.
TypedefsTest.o:(.rodata._ZTI18Typedefs_Sqrt_Test[_ZTI18Typedefs_Sqrt_Test]+0x10): undefined reference to `typeinfo for testing::Test'
TypedefsTest.o:(.rodata._ZTI17Typedefs_Sqr_Test[_ZTI17Typedefs_Sqr_Test]+0x10): undefined reference to `typeinfo for testing::Test'
collect2: error: ld returned 1 exit status
make: *** [all] Error 1
```

```
map479-admin@eee320:~/github/gesture_recognition_toolkit/examples/Tutorials/CustomMakefile$ make
----------------- Building GRT Example -----------------
g++ -c main.cpp -I/usr/local/include -g -O2 -Wall -L/usr/local/lib
In file included from /usr/local/include/GRT/GRT.h:84:0,
                 from main.cpp:33:
/usr/local/include/GRT/CoreAlgorithms/GridSearch/GridSearch.h:79:35: error: expected ‘)’ before ‘<’ token
     GridSearchParam( std::function< bool(T) > func = nullptr, GridSearchRange<T> range = GridSearchRange<T>() ){
                                   ^
```
