# Lua Stack Overflow Error with Recursive Table Iteration

This repository demonstrates a stack overflow error that can occur in Lua when a recursive function modifies a table while iterating over it using `pairs`. The bug is caused by the fact that `pairs` iterator doesn't handle table modifications gracefully.

## Bug Description

The `bug.lua` file contains a simple recursive function that iterates over a table and attempts to modify it.  This modification during iteration using `pairs` leads to unpredictable behavior and, in this case, a stack overflow error.

## Solution

The `bugSolution.lua` file provides a corrected version. The solution involves iterating over a copy of the table to prevent unexpected behavior, avoiding the modification during iteration.

## How to reproduce

1. Clone this repository.
2. Run `bug.lua` using a Lua interpreter.
3. Observe the stack overflow error. 
4. Run `bugSolution.lua` to see the corrected behavior.
