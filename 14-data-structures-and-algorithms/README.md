# 14 — Data Structures and Algorithms

## Learning goals
- Estimate complexity and implement searching, sorting, and common structures.

## Core concepts
Big-O describes growth as input grows. Linear search is O(n); binary search is O(log n) on sorted data. Test correctness and edge cases before optimizing.

## Example / practice prompt
Implement binary search using low/high bounds and a midpoint calculated as low + (high-low)/2.

## Exercises
1. Compare linear and binary search
2. implement insertion sort
3. build stack/queue
4. explain O(1), O(log n), O(n), O(n²).

## Completion checklist
- [ ] I can explain the key concepts without reading the lesson.
- [ ] I wrote and ran code related to this topic.
- [ ] I tested boundary cases and corrected any compiler warnings.
- [ ] I can explain one mistake I made and how I fixed it.

## Code examples

**C — linear search**
```c
#include <stdio.h>
int find_index(const int values[], int length, int target) {
    for (int i = 0; i < length; ++i)
        if (values[i] == target) return i;
    return -1;
}
int main(void) {
    int values[] = {4, 7, 2, 9};
    printf("Index: %d\\n", find_index(values, 4, 2));
    return 0;
}
```

**C++ — sort then binary search**
```cpp
#include <algorithm>
#include <iostream>
#include <vector>
int main() {
    std::vector<int> values{4, 7, 2, 9};
    std::sort(values.begin(), values.end());
    std::cout << std::boolalpha
              << std::binary_search(values.begin(), values.end(), 7) << '\\n';
}
```
