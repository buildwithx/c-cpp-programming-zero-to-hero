# 10 — Modules and Builds

## Learning goals
- Split code into headers/source files and understand compilation and linking.

## Core concepts
A translation unit is compiled separately, then the linker combines object files and libraries. Keep declarations and definitions consistent.

## Example / practice prompt
Example layout: include/calculator.h, src/calculator.c, src/main.c. Compile both source files in one gcc command.

## Exercises
1. Move a function into another source file
2. add include guards
3. build a three-file program
4. explain compiler versus linker.

## Completion checklist
- [ ] I can explain the key concepts without reading the lesson.
- [ ] I wrote and ran code related to this topic.
- [ ] I tested boundary cases and corrected any compiler warnings.
- [ ] I can explain one mistake I made and how I fixed it.

## Code examples

**C — separate header and source files**

`math_utils.h`
```c
#ifndef MATH_UTILS_H
#define MATH_UTILS_H
int add(int a, int b);
#endif
```

`math_utils.c`
```c
#include "math_utils.h"
int add(int a, int b) { return a + b; }
```

`main.c`
```c
#include <stdio.h>
#include "math_utils.h"
int main(void) { printf("%d\n", add(2, 3)); return 0; }
```
Compile: `gcc -std=c17 main.c math_utils.c -o app`.

**C++ — declaration and definition**
`greeter.hpp`
```cpp
#pragma once
#include <string>
std::string greeting();
```
`greeter.cpp`
```cpp
#include "greeter.hpp"
std::string greeting() { return "Hello from another file"; }
```
