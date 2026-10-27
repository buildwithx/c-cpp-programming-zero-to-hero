# 13 — Templates and Modern C++

## Learning goals
- Use templates, lambdas, auto, range-based loops, and move-aware types.

## Core concepts
Templates enable type-safe generic code. Lambdas create callables. Use auto when the initializer makes the type clear. Learn move semantics without assuming every move is cheap.

## Example / practice prompt
C++: template<class T> T larger(T a,T b){ return a < b ? b : a; }

## Exercises
1. Write a generic smaller function
2. sort with a lambda
3. explain auto deduction
4. research lvalues, rvalues, and std::move.

## Completion checklist
- [ ] I can explain the key concepts without reading the lesson.
- [ ] I wrote and ran code related to this topic.
- [ ] I tested boundary cases and corrected any compiler warnings.
- [ ] I can explain one mistake I made and how I fixed it.

## Code examples

**C++ — function template and lambda**
```cpp
#include <algorithm>
#include <iostream>
#include <vector>
template <typename T>
T larger(T a, T b) { return a < b ? b : a; }
int main() {
    std::vector<int> values{5, 1, 8, 3};
    std::sort(values.begin(), values.end(),
              [](int a, int b) { return a > b; });
    std::cout << "Larger: " << larger(10, 42) << '\\n';
    for (int value : values) std::cout << value << ' ';
}
```
