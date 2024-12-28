# Elixir Enum.each List Modification Bug

This example demonstrates a common misconception when working with lists and `Enum.each` in Elixir.  Many programmers from imperative backgrounds expect `List.delete` to modify the original list in place.  This is not how Elixir's immutable data structures work.

The `bug.exs` file contains code that attempts to remove the element `3` from a list within an `Enum.each` loop.  The `bugSolution.exs` file shows the correct approach to achieve this.

## How to reproduce

1.  Save the code in `bug.exs`.
2.  Run it from your Elixir shell: `elixir bug.exs`
3.  Observe that the original list remains unchanged despite the `List.delete` call inside the loop. 