# 03 — Control Flow

## Learning goals
- Write branches, loops, and switch statements.

## Core concepts
if/else handles conditions; switch selects among constant cases; for and while repeat work. Make loop progress explicit and watch off-by-one errors.

## Example / practice prompt
C++: for (int i=1; i<=5; ++i) std::cout << i << '\\n';

## Exercises
1. Print 1–100
2. create a guessing game
3. print a multiplication table
4. validate input until it is in range.

## Completion checklist
- [ ] I can explain the key concepts without reading the lesson.
- [ ] I wrote and ran code related to this topic.
- [ ] I tested boundary cases and corrected any compiler warnings.
- [ ] I can explain one mistake I made and how I fixed it.

## Code examples

**C — loop and condition**
```c
#include <stdio.h>
int main(void) {
    for (int n = 1; n <= 10; ++n) {
        if (n % 2 == 0) printf("%d is even\\n", n);
        else printf("%d is odd\\n", n);
    }
    return 0;
}
```

**C++ — switch**
```cpp
#include <iostream>
int main() {
    int choice{};
    std::cout << "1=Start 2=Help 0=Exit: ";
    if (!(std::cin >> choice)) return 1;
    switch (choice) {
        case 1: std::cout << "Starting\\n"; break;
        case 2: std::cout << "Help\\n"; break;
        case 0: std::cout << "Goodbye\\n"; break;
        default: std::cout << "Unknown choice\\n";
    }
}
```
