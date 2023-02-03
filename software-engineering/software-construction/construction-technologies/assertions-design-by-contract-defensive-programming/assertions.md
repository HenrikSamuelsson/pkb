# Assertions

An assertion is a Boolean expression that is expected to always be true at a specific point in a program execution. Should the assertion not be true so is there an error in the program code.

It is good practice to add assertions to the code during the development phase attempting to catch mistakes in the code. Should the assertion turn out to be evaluated as false so will the code execution be stopped and the line of code that caused the assertion to fail is reported.

The assertions is special code and is usually only activated in development version of the code and disabled when the code reaches the release stage. This means that should an assertion fail when run in release so will the program continue to execute and hopefully so will the failed assertion not cause an major issues.
