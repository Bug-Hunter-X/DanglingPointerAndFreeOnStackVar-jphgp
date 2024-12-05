# Dangling Pointer and free() on Stack Variable in C

This repository demonstrates a common error in C programming involving the use of `free()` on a pointer to a stack-allocated variable.

## The Bug

The `bug.c` file contains code that attempts to free a pointer (`ptr`) that points to a variable (`x`) allocated on the stack. This results in undefined behavior and can lead to crashes or other unpredictable outcomes.  The core issue is misuse of `free()`, which is intended for heap-allocated memory.

## The Solution

The `bugSolution.c` file demonstrates the correct approach. It avoids calling `free()` on the stack-allocated variable.