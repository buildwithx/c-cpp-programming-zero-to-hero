# 11 — Object-Oriented C++

## Learning goals
- Design classes, constructors, encapsulation, and object relationships.

## Core concepts
Keep data private and expose operations that preserve valid state. Prefer composition over inheritance unless an is-a relationship is genuine. RAII ties resources to object lifetime.

## Example / practice prompt
C++: class Counter { public: void increment(){ ++value_; } int value() const { return value_; } private: int value_{}; };

## Exercises
1. Build a BankAccount
2. enforce valid initialization
3. model a library
4. explain public/private and const methods.

## Completion checklist
- [ ] I can explain the key concepts without reading the lesson.
- [ ] I wrote and ran code related to this topic.
- [ ] I tested boundary cases and corrected any compiler warnings.
- [ ] I can explain one mistake I made and how I fixed it.
