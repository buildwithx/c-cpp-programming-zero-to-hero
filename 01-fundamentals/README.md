# 01 — Fundamentals

## Learning goals
- Understand statements, variables, types, initialization, and console I/O.

## Core concepts
C commonly uses int, double, and char. C++ also offers std::string. Initialize variables and check whether input operations succeed.

## Example / practice prompt
C: int age = 0; printf("%d", age); C++: int age{}; std::cout << age;

## Exercises
1. Print several types
2. read two numbers
3. build a temperature converter
4. explain why initialization matters.

## Completion checklist
- [ ] I can explain the key concepts without reading the lesson.
- [ ] I wrote and ran code related to this topic.
- [ ] I tested boundary cases and corrected any compiler warnings.
- [ ] I can explain one mistake I made and how I fixed it.

## Code examples

**C — input and variables**
```c
#include <stdio.h>
int main(void) {
    int age = 0;
    printf("Enter age: ");
    if (scanf("%d", &age) != 1) {
        fprintf(stderr, "Invalid input\n");
        return 1;
    }
    printf("Next year: %d\n", age + 1);
    return 0;
}
```

**C++ — input and variables**
```cpp
#include <iostream>
int main() {
    int age{};
    std::cout << "Enter age: ";
    if (!(std::cin >> age)) {
        std::cerr << "Invalid input\n";
        return 1;
    }
    std::cout << "Next year: " << age + 1 << '\n';
}
```
