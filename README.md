# Lua Nested Table Iteration Issue

This repository demonstrates a subtle issue related to the iteration order of Lua's `pairs` function when dealing with nested tables. The `pairs` iterator does not guarantee a specific order, which can lead to unexpected results when recursively traversing tables.

The `bug.lua` file contains code that recursively iterates through a nested table.  Due to the unpredictable order of `pairs`, the processing order of nested elements may vary across different Lua implementations or even on different runs of the same code.

The `bugSolution.lua` file provides a possible solution illustrating how to maintain a consistent order using a sorted iteration approach if needed.

## Reproducing the Bug

1. Clone the repository.
2. Run `bug.lua` using a Lua interpreter.
3. Observe that the output might vary upon each run.