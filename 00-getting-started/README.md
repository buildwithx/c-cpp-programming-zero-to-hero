# 00 — Getting Started

## Learning goals
- Understand source code, compilers, and executables
- build your first C and C++ programs.

## Core concepts
Source code is translated by a compiler into an executable. The workflow is edit, compile, inspect diagnostics, run, and iterate.

## Example / practice prompt
Create hello.c with printf and hello.cpp with std::cout. Compile with gcc -std=c17 and g++ -std=c++17, enabling -Wall -Wextra -Wpedantic.

## Exercises
1. Change the greeting
2. print three lines
3. intentionally cause and fix a compiler error
4. explain source code versus executable.

## Completion checklist
- [ ] I can explain the key concepts without reading the lesson.
- [ ] I wrote and ran code related to this topic.
- [ ] I tested boundary cases and corrected any compiler warnings.
- [ ] I can explain one mistake I made and how I fixed it.

## Code examples

**C — `hello.c`**
```c
#include <stdio.h>
int main(void) {
    printf("Hello from C!\\n");
    return 0;
}
```
Compile: `gcc -std=c17 -Wall -Wextra -Wpedantic hello.c -o hello`

**C++ — `hello.cpp`**
```cpp
#include <iostream>
int main() {
    std::cout << "Hello from C++!\\n";
}
```
Compile: `g++ -std=c++17 -Wall -Wextra -Wpedantic hello.cpp -o hello`
