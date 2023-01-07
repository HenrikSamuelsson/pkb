---
tags: software-testing, fuzzing 
---
# Fuzzing

Fuzzing or fuzz testing is an automated software testing technique that involves providing random data as inputs to a computer program. The program is then monitored for exceptions such as crashes, failing built-in code assertions, or potential memory leaks. Typically, fuzzing is used to test programs that take structured inputs. This structure is specified, e.g., in a file format or protocol and distinguishes valid from invalid input. Effective fuzzing generates semi-valid inputs that are "valid enough" in that they are not directly rejected by the parser, but do create unexpected behaviors deeper in the program and are "invalid enough" to expose corner cases that have not been properly dealt with.

One fuzzing library is [libFuzzer](https://llvm.org/docs/LibFuzzer.html) is a fuzzing that is part of the LLVM project. It is a compiler-aided fuzzer. It is the default go-to fuzzer if your project is already compilable with the LLVM toolchain, since using libFuzzer only requires an additional compiler/linker flag and defining a single function.

Another notable fuzzer is [AFLplusplus](https://github.com/AFLplusplus/AFLplusplus)
