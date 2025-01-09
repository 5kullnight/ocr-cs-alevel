Variables can be defined with either **global** or **local** scope. Scope refers to the section of code in which the variable is available.
#### Local Variables
- **Definition**: Local variables have limited scope and can only be accessed within the block of code where they were defined.
- **Accessibility**: If a local variable is defined within a subroutine, it can only be accessed within that subroutine.
- **Name Collision**: Multiple local variables with the same name can exist in different subroutines without affecting each other.
- **Best Practices**: Using local variables is considered good programming practice because it ensures subroutines are self-contained, minimizing the risk of variables being affected by code outside the subroutine.
#### Global Variables
- **Definition**: Global variables can be accessed across the entire program.
- **Automatic Declaration**: All variables used in the main body of a program are automatically declared as global.
- **Use Cases**: Global variables are useful for values that need to be used by multiple parts of the program.
- **Drawbacks**:
    - Global variables are not recommended for general use because they can be unintentionally overwritten and modified.
    - They remain in memory until the program terminates, requiring more memory than local variables, which are deleted once the subroutine has completed.
#### Precedence
In the event that a local variable exists within a subroutine with the same name as a global variable, the local variable will take precedence.