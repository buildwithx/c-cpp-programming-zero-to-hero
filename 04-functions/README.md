# 04 — Functions

## Learning goals
- Create reusable functions and understand parameters, return values, scope, and recursion.

## Core concepts
A function gives a named operation a clear interface. Keep functions focused. In C, provide declarations before use; C++ also supports overloading.

## Example / practice prompt
C++: int square(int value) { return value * value; }

## Exercises
1. Write min/max functions
2. test primality
3. implement factorial iteratively and recursively
4. explain parameter versus argument.

## Completion checklist
- [ ] I can explain the key concepts without reading the lesson.
- [ ] I wrote and ran code related to this topic.
- [ ] I tested boundary cases and corrected any compiler warnings.
- [ ] I can explain one mistake I made and how I fixed it.

## Code examples

**C — reusable function**
```c
#include <stdio.h>
int maximum(int a, int b) { return a > b ? a : b; }
int main(void) {
    printf("Maximum: %d\\n", maximum(12, 7));
    return 0;
}
```

**C++ — reference parameter**
```cpp
#include <iostream>
void double_value(int& value) { value *= 2; }
int main() {
    int score = 21;
    double_value(score);
    std::cout << score << '\\n'; // 42
}
```
