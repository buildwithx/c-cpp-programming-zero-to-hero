# 17 — Advanced Topics

## Learning goals
- Explore concurrency, performance, and larger project design.

## Core concepts
Learn concurrency after understanding shared state and object lifetime. Measure performance before optimizing. Study language standards and confirm which version introduced a feature.

## Example / practice prompt
Next topics: C undefined behavior and function pointers; C++ move semantics, concepts, ranges, concurrency; CMake, GDB/LLDB, sanitizers, static analysis, CI.

## Exercises
1. Profile before/after one optimization
2. compare compiler diagnostics
3. build a thread-safe example after studying synchronization
4. summarize an advanced topic.

## Completion checklist
- [ ] I can explain the key concepts without reading the lesson.
- [ ] I wrote and ran code related to this topic.
- [ ] I tested boundary cases and corrected any compiler warnings.
- [ ] I can explain one mistake I made and how I fixed it.

## Code examples

**C++ — synchronized shared state**
```cpp
#include <iostream>
#include <mutex>
#include <thread>
int main() {
    int total = 0;
    std::mutex mutex;
    auto work = [&]() {
        for (int i = 0; i < 1000; ++i) {
            std::lock_guard<std::mutex> lock(mutex);
            ++total;
        }
    };
    std::thread first(work), second(work);
    first.join();
    second.join();
    std::cout << total << '\n'; // 2000
}
```
Compile where pthread flags are required: `g++ -std=c++17 -pthread main.cpp -o main`. This introduces synchronization; study data races and lock scope before building larger concurrent programs.
