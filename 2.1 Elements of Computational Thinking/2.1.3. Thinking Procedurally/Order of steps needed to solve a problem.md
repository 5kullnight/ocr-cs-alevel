When constructing the final solution based on the solutions to the problem components, thinking about the order in which operations are performed becomes important. Some programs might require certain inputs to be entered by the user before the processing can be carried out. These inputs would also need to be validated before they can be passed onto the next subroutines, which must also be taken into consideration.
It might be possible for several subroutines to be executed simultaneously within a program, and programmers must identify where this is possible by looking at the data and inputs the subroutine requires. Some subroutines will require data from other subroutines before they are able to execute, and so will be unable to execute simultaneously. In this case, programmers should determine the order in which subroutines are executed, as well as how they interact with each other, based on their role in solving the problem.

---
# Example: Book Reservation System
Going back to our earlier example involving a **book reservation system**, it is clear that certain operations must be performed before others can be performed. Without the user’s input, the rest of the program cannot execute. There must also be checks in place to confirm the validity of these inputs before data is passed between subroutines.

---
# Example: Game Design
The same principle is important when considering how a program will be used. Programs should be built to ensure operations are not carried out in an order that does not make sense or will raise an error. Consider an **adventure game**. It should not be possible for users to access and play levels ahead of those they have unlocked.

---
# Example: Food Delivery App
A **fast food delivery app** should not allow users to select food until they have confirmed their location, nor should it allow users to pay before they have confirmed their order. Although these things may seem obvious and natural to us, they must be explicitly written into software for programs to work in the way we want.