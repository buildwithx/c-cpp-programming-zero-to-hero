# 07 — Structs, Enums, and Types

## Learning goals
- Group data and use enums and aliases to communicate intent.

## Core concepts
A struct groups related fields. Enums model a fixed set of choices. C++ enum class prevents many accidental implicit conversions.

## Example / practice prompt
C++: enum class Status { pending, complete }; struct Task { std::string title; Status status{Status::pending}; };

## Exercises
1. Model a student
2. represent traffic lights
3. print a C struct
4. explain useful type aliases.

## Completion checklist
- [ ] I can explain the key concepts without reading the lesson.
- [ ] I wrote and ran code related to this topic.
- [ ] I tested boundary cases and corrected any compiler warnings.
- [ ] I can explain one mistake I made and how I fixed it.

## Code examples

**C — struct and enum**
```c
#include <stdio.h>
enum Status { PENDING, COMPLETE };
struct Task { int id; enum Status status; };
int main(void) {
    struct Task task = {1, PENDING};
    printf("Task %d: %s\\n", task.id,
           task.status == COMPLETE ? "complete" : "pending");
    return 0;
}
```

**C++ — scoped enum and struct**
```cpp
#include <iostream>
#include <string>
enum class Status { pending, complete };
struct Task { int id; std::string title; Status status{Status::pending}; };
int main() {
    Task task{1, "Study types"};
    std::cout << task.id << ": " << task.title << '\\n';
}
```
