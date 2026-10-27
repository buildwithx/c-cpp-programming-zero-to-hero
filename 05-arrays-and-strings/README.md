# 05 — Arrays and Strings

## Learning goals
- Index arrays safely and handle C strings and C++ strings.

## Core concepts
Array indices start at zero. C arrays do not carry their length. C strings end with a null character; in C++, prefer std::string for text.

## Example / practice prompt
C++: std::string name; std::getline(std::cin, name); std::cout << name;

## Exercises
1. Find array min/max
2. reverse an array
3. count vowels
4. explain why C strings should be compared with strcmp, not ==.

## Completion checklist
- [ ] I can explain the key concepts without reading the lesson.
- [ ] I wrote and ran code related to this topic.
- [ ] I tested boundary cases and corrected any compiler warnings.
- [ ] I can explain one mistake I made and how I fixed it.

## Code examples

**C — array length and sum**
```c
#include <stdio.h>
int main(void) {
    int values[] = {4, 8, 2, 9, 3};
    size_t length = sizeof values / sizeof values[0];
    int sum = 0;
    for (size_t i = 0; i < length; ++i) sum += values[i];
    printf("Count=%zu, sum=%d\\n", length, sum);
    return 0;
}
```

**C++ — string and range loop**
```cpp
#include <iostream>
#include <string>
int main() {
    std::string word = "programming";
    int vowels = 0;
    for (char ch : word)
        if (ch=='a'||ch=='e'||ch=='i'||ch=='o'||ch=='u') ++vowels;
    std::cout << vowels << " vowels\\n";
}
```
