# 2.0 Beginning the Coding Adventure: Your First Program
## 2.1 Writing Your First Program
First, define your expectations for the program. This type of structured and semi-formal description of each step of the program is called an **algorithm**.

```txt
#include <iostream>
using namespace std;

int main(void) {
  cout << "Hello, world!" << endl;
  return 0;
}
```

We'll go line by line to explain the code.

- `#include` is a **preprocessor directive**, which is a separate part of the compiler who pre-read the text of the program to make modification in it.
- `<iostream>` is the standard header that provides input/output facilities (notably `std::cout` and `std::endl`). Without this directive, the compiler won't know what `cout` and `endl` are.

A set of preliminary information that the compiler needs is included in **header files**. these files contain a collection of preliminary information about ready-made blocks which can be used by a program to write text on the screen, or to read input rom the keyboard. So, when out program is goin to output something to the console, it will use the block called cout.

- `using namespace std;` In the C++ language, all elements of the standard C++ library are declared inside the namespace called `std`.

A **namespace** is an abstract container or environment created to hold a logical grouping of unqiue entities (blocks). An entity defined in a namespace is associated only with that namespace. Allows you to write `cout` instead of `std::cout`.

One of the most common types of blocks used to build C++ programs are **functions**. Imagine a function as a black box, which you can insert something into and take something new out of it. Things put into a function are called **function arguments** (**parameters**) and things output by a function are called **function results**. The standard C++ language assumes that one specific block, or function, must always be present, i.e., `main`.

- `int main(void)` indicates that the `main` function will return an **integer** (typically returns `0` to indicate success) and takes no paramters (as suggested by `void`).
- `{` begins the function body which is a block of code that runs when the program starts.

Every function in C++ begins with the following set of informaiton:
- What is the result of the function?
- What is the name of the function?
- How many parameters does the function have and what are their names?

This set of information is sometimes called a **prototype** which is like a label affixed to a function announcing how you can use that function in your program.

The function doesn't have to take any paramters nor anything into the body.

``` txt
void laxy(void) { }
```

Inside the main function body we write what our function (and thus the program) should do.

- `cout` is a reference to the block (entity) for the standard (`std`) output stream (console output)
- `<<` this digraph is the **stream insertion operator** which sends data to the stream.
- `"Hello, world!"` is a string literal which is text in double quotes stored in the program's read-only memory
- `<< endl;` means "end of line" and inserts a newline character and flushes the output buffer to ensure output appears immediately.

The follwoing is the final statement within the code.
-`return 0;` ends the `main` function and returns the value `0` to the operating system. The `0` indicates that the program was sucessful, otherwise the console would output some kind of error/failure code.
-`}` ends the `main` function body.
