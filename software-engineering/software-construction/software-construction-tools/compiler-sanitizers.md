---
tags: c, cpp, sanitizer, clang, gcc, llvm
---
# Compiler Sanitizers

Some C/C++ compilers support a concept called sanitizers. A sanitizer will track the execution at runtime and report execution errors. This means that the sanitizer must be built into the application and it will consume some extra resources.

Examples of sanitizers and error detection capability:

- Address sanitizer and leak sanitizer
  - Use after free (dangling pointer dereference)
  - Heap buffer overflow
  - Stack buffer overflow
  - Global buffer overflow
  - Use after return
  - Use after scope
  - Initialization order bugs
  - Memory leaks
- Thread sanitizer
  - Data race detection
- Memory sanitizer
  - Uninitialized memory reads

The C/C++ compilers Clang/LLVM and GCC are among the compilers that have support for sanitizers.
