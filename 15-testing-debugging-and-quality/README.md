# 15 — Testing, Debugging, and Quality

## Learning goals
- Use warnings, debuggers, tests, and sanitizers.

## Core concepts
Compile with warnings enabled. A debugger lets you step and inspect state. Test normal cases, boundaries, empty input, and invalid input. Sanitizers can catch memory errors during development.

## Example / practice prompt
Compile with -g -Wall -Wextra -Wpedantic. On supported GCC/Clang systems, try -fsanitize=address,undefined.

## Exercises
1. Write calculator tests
2. debug an off-by-one error
3. test empty arrays
4. document reproduction steps for a bug.

## Completion checklist
- [ ] I can explain the key concepts without reading the lesson.
- [ ] I wrote and ran code related to this topic.
- [ ] I tested boundary cases and corrected any compiler warnings.
- [ ] I can explain one mistake I made and how I fixed it.

## Code examples

**C — assertions**
```c
#include <assert.h>
int add(int a, int b) { return a + b; }
int main(void) {
    assert(add(2, 3) == 5);
    assert(add(-2, 2) == 0);
    assert(add(0, 0) == 0);
    return 0;
}
```

**C++ — simple checks**
```cpp
#include <cassert>
int square(int value) { return value * value; }
int main() {
    assert(square(0) == 0);
    assert(square(3) == 9);
    assert(square(-4) == 16);
}
```
Standard `assert` checks may be disabled when `NDEBUG` is defined.
