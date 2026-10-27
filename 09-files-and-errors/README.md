# 09 — Files and Errors

## Learning goals
- Read and write files and handle failures deliberately.

## Core concepts
File operations can fail. Check return values. C uses FILE* and fopen/fclose; C++ offers ifstream/ofstream.

## Example / practice prompt
C++: std::ifstream in("notes.txt"); if (!in) { std::cerr << "Cannot open file"; return 1; }

## Exercises
1. Write lines to a file
2. count words
3. handle invalid input
4. explain why file handles need cleanup.

## Completion checklist
- [ ] I can explain the key concepts without reading the lesson.
- [ ] I wrote and ran code related to this topic.
- [ ] I tested boundary cases and corrected any compiler warnings.
- [ ] I can explain one mistake I made and how I fixed it.
