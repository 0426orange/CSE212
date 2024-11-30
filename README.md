# Final
# Stacks

## Introduction
A stack is a data structure that follows the **Last In, First Out (LIFO)** principle. Think of it like a stack of plates at a buffet: the last plate you put on the stack is the first one you take off. This makes stacks useful for scenarios where the order of operations matters, such as undo features in software or evaluating mathematical expressions.

## Characteristics
- **LIFO Behavior:** The last element added to the stack is the first to be removed.
- Common operations include:
  - **Push:** Add an element to the top of the stack.
  - **Pop:** Remove the top element.
  - **Peek:** View the top element without removing it.
  - **IsEmpty:** Check if the stack is empty.

## Strengths and Use Cases
Stacks are excellent for:
- **Reversing data** (e.g., reversing a string or list).
- **Backtracking** in algorithms like maze-solving or parsing.
- **Managing operations** such as function calls or undo mechanisms.

## Example: Backtracking in Maze Navigation
Imagine a robot exploring a maze. The robot can use a stack to keep track of its path. If it hits a dead end, it can backtrack by popping the last position off the stack.

```csharp
using System;
using System.Collections.Generic;

class MazeSolver
{
    public static void NavigateMaze()
    {
        Stack<string> path = new Stack<string>();
        path.Push("Start");
        path.Push("Move to (1,1)");
        path.Push("Move to (2,1)");
        path.Push("Dead End at (3,1)");
        
        Console.WriteLine("Backtracking...");
        while (path.Count > 0)
        {
            Console.WriteLine($"Popping: {path.Pop()}");
        }
    }
}
