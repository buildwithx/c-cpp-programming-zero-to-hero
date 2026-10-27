# 16 — Projects

## Learning goals
- Combine concepts into complete programs with requirements and tests.

## Core concepts
Start small and increase complexity. Define requirements, divide work into functions, validate input, test edge cases, and document how to build and use the program.

## Example / practice prompt
Beginner: profile printer, unit converter, number guessing game. Intermediate: calculator, quiz app, contact book. Advanced: expense tracker, inventory manager, text analyzer, task manager capstone.

## Exercises
1. Choose one project
2. write requirements
3. implement a minimum viable version
4. add features incrementally
5. document build steps and tests.

## Completion checklist
- [ ] I can explain the key concepts without reading the lesson.
- [ ] I wrote and ran code related to this topic.
- [ ] I tested boundary cases and corrected any compiler warnings.
- [ ] I can explain one mistake I made and how I fixed it.

## Code examples

**C++ — small expense summary**
```cpp
#include <iomanip>
#include <iostream>
#include <vector>
int main() {
    std::vector<double> expenses;
    std::cout << "Enter 3 expenses:\\n";
    for (int i = 0; i < 3; ++i) {
        double amount{};
        if (!(std::cin >> amount) || amount < 0) {
            std::cerr << "Enter non-negative numbers.\\n";
            return 1;
        }
        expenses.push_back(amount);
    }
    double total = 0;
    for (double amount : expenses) total += amount;
    std::cout << std::fixed << std::setprecision(2)
              << "Total: " << total << '\\n';
}
```
Extend it with file persistence, categories, and tests.
