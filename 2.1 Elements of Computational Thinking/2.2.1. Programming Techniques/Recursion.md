Recursion is a programming construct in which a subroutine calls itself during its execution. This continues until a certain condition — called the **stopping condition** — is met, at which point the recursion stops. Recursion produces the same result as iteration but is more suited to certain problems that are more easily expressed using recursion.
#### Advantages of Recursion
- **Conciseness**: Problems can be represented in fewer lines of code, making them less prone to errors.
- **Natural Representation**: Some problems are more naturally expressed using recursive solutions.
#### Important Considerations
- It is essential that recursive subroutines are clearly defined to reach a stopping condition after a finite number of function calls.
#### Example: Factorial Function
A common example of a naturally recursive function is the factorial function:
```
function factorial(number)
    if number == 0 or 1:
        return 1
    else:
        return number * factorial(number - 1)
    endif
end function
```
Each time the function calls itself, a new **stack frame** is created within the call stack, where parameters, local variables, and return addresses are stored. This information allows the subroutine to return to that particular point during its execution. A finite number of stack frames are created until the stopping condition (or **base case**) is reached, at which point the subroutine unwinds. This refers to the process of information from the call stack being popped off the stack.
#### Disadvantages of Recursion
- **Inefficient Memory Use**: Recursion can be memory-intensive, leading to stack overflow if the subroutine calls itself too many times, causing the program to crash.
- **Difficult to Trace**: Tracing recursive calls can be challenging, especially as the number of function calls increases.
#### Tail Recursion
Tail recursion is a form of recursion that is implemented in a more efficient way, requiring less stack space.