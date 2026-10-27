# 08 — Memory and Lifetime

## Learning goals
- Understand object lifetime and avoid leaks and invalid memory access.

## Core concepts
C dynamic allocation must be paired with free. Modern C++ prefers RAII, standard containers, and smart pointers over manual new/delete.

## Example / practice prompt
C: int *p = malloc(10 * sizeof *p); check p != NULL; use it; free(p). Include stdlib.h.

## Exercises
1. Draw local-variable lifetimes
2. allocate/free an array in C
3. replace an owning raw pointer with vector or unique_ptr
4. explain RAII.

## Completion checklist
- [ ] I can explain the key concepts without reading the lesson.
- [ ] I wrote and ran code related to this topic.
- [ ] I tested boundary cases and corrected any compiler warnings.
- [ ] I can explain one mistake I made and how I fixed it.
