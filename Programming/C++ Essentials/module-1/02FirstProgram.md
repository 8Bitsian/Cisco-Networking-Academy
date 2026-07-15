# 2.0 Beginning the Coding Adventure: Your First Program
## 2.0.1 Writing Your First Program
First, define your expectations for the program. This type of structured and semi-formal description of each step of the program is called an **algorithm**.

```txt
#include <iostream>
using namespace std

int main(void) {
  cout << "Hello, world!" << endl;
  return 0;
}
```

We'll go line by line to explain the code.

- `#include` is a **preprocessor directive**, which is a separate part of the compiler who pre-read the text of the program to make modification in it.
- `<iostream>` is the standard header that provides input/output facilities (notably `std::cout` and `std::endl`).


Pay attention to the hash (#) at the beginning of the first line. It means that the content of this line is the **preprocessor directive**. It is a separate part of the compiler whose task is to pre-read the text of the program and make some modifications in it. The prefix "pre" suggests that these operations are performed before the full processing (compilation) takes place.

The changes the **preprocessor** will introduction are fully controlled by its directives.
