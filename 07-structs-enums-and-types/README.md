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
