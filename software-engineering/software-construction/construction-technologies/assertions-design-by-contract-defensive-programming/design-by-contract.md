---
tags: design-by-contract, precondition, side-effect, postcondition, invariant, assertion
---
# Design By Contract

Design by contract (DbC) is an approach in software design that prescribes that component interfaces should have clearly stated preconditions, side effects, postconditions, and invariants.

Precondition is an action that needs have been executed before calling the interface. Examples of preconditions is that different types of configuration and initialization shall have been completed.

Side effects means that the state of a variable is modified outside of the local environment. It is better if an interface do not have any side effects at all, but if it do have side effects this should be documented.

Postcondition is condition guaranteed to be true after a interface method have executed. These are about what the component itself is responsible for. For example, the result of a factorial is always an integer and greater than or equal to 1.

An invariant is a logical assertion that is always held to be true during a certain phase of execution of a computer program. For example, a loop invariant is a condition that is true at the beginning and the end of every iteration of a loop.

Design by contract can be verified by adding assertions to the code.
