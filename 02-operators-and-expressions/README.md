# 02 — Operators and Expressions

## Learning goals
- Use arithmetic, comparison, logical operators, precedence, and conversions.

## Core concepts
Integer division discards the fractional part. Use explicit conversions when floating-point results are needed. Parentheses make intent clearer.

## Example / practice prompt
C++: int a=7,b=2; std::cout << a/b << ' ' << static_cast<double>(a)/b;

## Exercises
1. Build a calculator
2. test divisibility by 3 and 5
3. convert seconds to h:m:s
4. predict mixed-type expressions.

## Completion checklist
- [ ] I can explain the key concepts without reading the lesson.
- [ ] I wrote and ran code related to this topic.
- [ ] I tested boundary cases and corrected any compiler warnings.
- [ ] I can explain one mistake I made and how I fixed it.

## Code examples

**C — arithmetic**
```c
#include <stdio.h>
int main(void) {
    int a = 17, b = 5;
    printf("sum=%d, quotient=%d, remainder=%d\n", a+b, a/b, a%b);
    printf("floating quotient=%.2f\n", (double)a/b);
    return 0;
}
```

**C++ — explicit conversion**
```cpp
#include <iostream>
int main() {
    int a = 17, b = 5;
    std::cout << a / b << '\n';
    std::cout << static_cast<double>(a) / b << '\n';
}
```
