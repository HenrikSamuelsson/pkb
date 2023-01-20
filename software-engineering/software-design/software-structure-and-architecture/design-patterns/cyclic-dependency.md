---
tags: antipattern 
---
# Cyclic Dependency

A cyclic dependency (aka circular dependency) is an antipattern that we try to avoid in software architecture.

> A cyclic dependency is formed when two or more abstractions have direct or indirect dependencies on each other. Cyclic dependencies between abstractions violate the Acyclic Dependencies Principle (ADP)[79] and Ordering Principle [80]. In the presence of cyclic dependencies, the abstractions that are cyclically-dependent may need to be understood, changed, used, tested, or reused together. Further, in case of cyclic dependencies, changes in one class (say A) may lead to changes in other classes in the cycle (say B). However, because of the cyclic nature, changes in B can have ripple effects on the class where the change originated (i.e., A). Large and indirect cyclic dependencies are usually difficult to detect in complex software systems and are a common source of subtle bugs. Since this smell is a result of not adhering to the enabling technique, “create acyclic dependencies,” we name this smell Cyclically dependent Modularization.

The above is a quoted from the book Refactoring for Software Design Smells, Managing Technical Debt.
