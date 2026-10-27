# 09 — Files and Errors

## Learning goals
- Read and write files and handle failures deliberately.

## Core concepts
File operations can fail. Check return values. C uses FILE* and fopen/fclose; C++ offers ifstream/ofstream.

## Example / practice prompt
C++: std::ifstream in("notes.txt"); if (!in) { std::cerr << "Cannot open file"; return 1; }

## Exercises
1. Write lines to a file
2. count words
3. handle invalid input
4. explain why file handles need cleanup.

## Completion checklist
- [ ] I can explain the key concepts without reading the lesson.
- [ ] I wrote and ran code related to this topic.
- [ ] I tested boundary cases and corrected any compiler warnings.
- [ ] I can explain one mistake I made and how I fixed it.

## Code examples

**C — write a file and check errors**
```c
#include <stdio.h>
int main(void) {
    FILE *file = fopen("message.txt", "w");
    if (file == NULL) { perror("message.txt"); return 1; }
    if (fprintf(file, "Learning C file I/O\\n") < 0) {
        perror("write"); fclose(file); return 1;
    }
    if (fclose(file) != 0) { perror("close"); return 1; }
    return 0;
}
```

**C++ — read a text file**
```cpp
#include <fstream>
#include <iostream>
#include <string>
int main() {
    std::ifstream input("message.txt");
    if (!input) { std::cerr << "Cannot open file\\n"; return 1; }
    std::string line;
    while (std::getline(input, line)) std::cout << line << '\\n';
}
```
