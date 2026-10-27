# C/C++ Programming: Zero to Hero

A folder-based, hands-on roadmap for learning **C and C++ from beginner to advanced**. Lessons are Markdown files with concepts, examples, exercises, and checklists.

> Recommended: learn the shared programming foundations, then treat C and C++ as distinct languages. C++ is not simply “C with classes.”

## Environment setup

Examples use **C17** and **C++17** unless noted. You need a compiler and terminal.

### macOS

Recommended: Apple Command Line Tools. Open Terminal and run:
```bash
xcode-select --install
clang --version
clang++ --version
```
Compile/run C: `clang -std=c17 -Wall -Wextra -Wpedantic main.c -o main && ./main`

Compile/run C++: `clang++ -std=c++17 -Wall -Wextra -Wpedantic main.cpp -o main && ./main`

Alternative: install Homebrew from https://brew.sh, then run `brew install gcc`. The GCC executable may be versioned; check `brew info gcc`.

### Windows

Recommended: MSYS2 with GCC.
1. Install MSYS2 from https://www.msys2.org.
2. Open **MSYS2 UCRT64** from the Start menu.
3. Update packages with `pacman -Syu`. If asked to close the terminal, reopen UCRT64 and repeat as instructed.
4. Install tools:
```bash
pacman -S --needed mingw-w64-ucrt-x86_64-gcc mingw-w64-ucrt-x86_64-gdb mingw-w64-ucrt-x86_64-make
```
5. Verify with `gcc --version` and `g++ --version`.
6. Compile C: `gcc -std=c17 -Wall -Wextra -Wpedantic main.c -o main.exe`; run `./main.exe`.
7. Compile C++: `g++ -std=c++17 -Wall -Wextra -Wpedantic main.cpp -o main.exe`; run `./main.exe`.

To use GCC from PowerShell or VS Code, add `C:\msys64\ucrt64\bin` to Windows `PATH`, then restart the terminal.

Alternative: install Visual Studio from https://visualstudio.microsoft.com and select **Desktop development with C++**. Use Developer PowerShell/Command Prompt; compile C++ with `cl /EHsc main.cpp` and run `.\main.exe`.

### Linux

Debian/Ubuntu:
```bash
sudo apt update
sudo apt install build-essential gdb
```
Fedora: `sudo dnf install gcc gcc-c++ gdb make`

Arch Linux: `sudo pacman -S --needed base-devel gdb`

Verify `gcc --version` and `g++ --version`. Compile C with `gcc -std=c17 -Wall -Wextra -Wpedantic main.c -o main`; compile C++ with `g++ -std=c++17 -Wall -Wextra -Wpedantic main.cpp -o main`. Run on macOS/Linux with `./main`.

### Optional editor and first check

Visual Studio Code is available at https://code.visualstudio.com. Its C/C++ extension helps with editing/debugging but does not replace a compiler.

Create `main.c`:
```c
#include <stdio.h>
int main(void) {
    printf("Hello, C!\n");
    return 0;
}
```
Create `main.cpp`:
```cpp
#include <iostream>
int main() {
    std::cout << "Hello, C++!\n";
}
```
Compile and run both. If both work, your environment is ready.

## Roadmap

| Stage | Folder | Topics |
|---:|---|---|
| 00 | [Getting started](00-getting-started/) | Source code, compiler, first program |
| 01 | [Fundamentals](01-fundamentals/) | Syntax, variables, types, I/O |
| 02 | [Operators](02-operators-and-expressions/) | Arithmetic, logic, conversions |
| 03 | [Control flow](03-control-flow/) | Conditions, loops, switch |
| 04 | [Functions](04-functions/) | Parameters, return values, scope |
| 05 | [Arrays and strings](05-arrays-and-strings/) | Arrays, C strings, std::string |
| 06 | [Pointers and references](06-pointers-and-references/) | Addresses, pointers, safety |
| 07 | [Structs, enums, types](07-structs-enums-and-types/) | User-defined types |
| 08 | [Memory and lifetime](08-memory-and-lifetime/) | Allocation, lifetime, RAII |
| 09 | [Files and errors](09-files-and-errors/) | File I/O, validation |
| 10 | [Modules and builds](10-modules-and-builds/) | Headers, compilation, linking |
| 11 | [Object-oriented C++](11-object-oriented-cpp/) | Classes, encapsulation, inheritance |
| 12 | [Standard library](12-standard-library/) | Containers, algorithms, smart pointers |
| 13 | [Templates and modern C++](13-templates-and-modern-cpp/) | Templates, lambdas, move semantics |
| 14 | [Data structures and algorithms](14-data-structures-and-algorithms/) | Big-O, searching, sorting |
| 15 | [Testing and quality](15-testing-debugging-and-quality/) | Debugging, tests, sanitizers |
| 16 | [Projects](16-projects/) | Guided projects |
| 17 | [Advanced topics](17-advanced-topics/) | Concurrency, performance, next steps |

## Study method

1. Follow lessons in order and type the examples yourself.
2. Predict output before running code.
3. Complete exercises independently and test edge cases.
4. Compile with warnings: `-Wall -Wextra -Wpedantic`.
5. Keep notes about errors and revisit exercises later.
6. Track your progress in [PROGRESS.md](PROGRESS.md).

See [CONTRIBUTING.md](CONTRIBUTING.md) for ways to improve the course. Licensed under MIT; see [LICENSE](LICENSE).
