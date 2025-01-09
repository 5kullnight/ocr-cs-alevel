**Modular programming** is a programming technique used to split large, complex programs into smaller, self-contained modules. Modularity is essential for making a problem easier to understand and approach. A modular design also facilitates task division among a team, simplifies management, and eases the testing and maintenance processes, as each component can be handled individually. This improves the reusability of components, allowing tested modules to be reused with confidence.
A popular technique used to modularize programs is the **top-down approach**, where the problem is continuously broken down into sub-problems until each can be represented as an individual, self-contained black box that performs a certain task. This process is also known as **stepwise refinement**. These modules form blocks of code called **subroutines**, which can be categorized as either **functions** or **procedures**.
#### Functions vs. Procedures
- **Subroutines** are named blocks of code that perform a specific task.
- **Procedures**:
    - Do not have to return a value.
    - Can return multiple values.
    - Typically receive data as parameters for manipulation.
- **Functions**:
    - Must always return a single value.
    - Commonly utilize local variables.
**Example of a Function**:
```
function isEven(number):
    if number MOD 2 = 0:
        return True
    else:
        return False
end function
```
#### Parameter Passing
When parameters are passed into a subroutine, they can be passed **by value** or **by reference**:
- **By Value**:
    - The parameter is treated as a local variable.
    - A copy of the value is passed to the subroutine and discarded at the end, meaning its value outside the subroutine remains unaffected.
- **By Reference**:
    - The address of the parameter is passed to the subroutine.
    - The value of the parameter will be updated at the given address.
**Note**: In exam questions, you should assume parameters are passed by value unless specified otherwise. The following format illustrates this:
```
function multiply(x: byVal, y: byRef)
```
