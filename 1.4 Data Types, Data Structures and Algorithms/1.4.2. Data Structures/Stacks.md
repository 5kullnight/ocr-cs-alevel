A **stack** is a data structure that follows the Last In, First Out (LIFO) principle, meaning the last element added to the stack is the first one to be removed. Stacks are crucial in computer science for various operations, such as reversing actions, managing function calls, and handling undo operations in applications.

---
### **Stack Operations**
Stacks can be manipulated using various operations, which are performed on the top of the stack. The following operations can be performed on a stack:

|**Operation**|**Syntax**|**Description**|**Example Output**|
|---|---|---|---|
|**isEmpty()**|`Stack.isEmpty()`|Checks if the stack is empty. Works by checking the top pointer value.|`True`|
|**push(value)**|`Stack.push("Nadia")`|Adds a new value to the top of the stack. Checks if the stack is not full before pushing.||
||`Stack.push("Elijah")`|||
|**peek()**|`Stack.peek()`|Returns the top value from the stack without removing it. Checks if the stack is not empty.|`"Elijah"`|
|**pop()**|`Stack.pop()`|Removes and returns the top value of the stack. Checks if the stack is not empty.|`"Elijah"`|
|**size()**|`Stack.size()`|Returns the current size of the stack.|`2`|
|**isFull()**|`Stack.isFull()`|Checks if the stack is full and returns a Boolean value. Compares the stack size to the top pointer.|`False`|

---
### **Implementation of Stacks**
Stacks can be implemented in two ways:
- **Static Stack:** Used when the maximum size is known in advance. It is easier to implement and uses memory more efficiently.
- **Dynamic Stack:** Allows for dynamic resizing as elements are added or removed, but is generally more complex to implement.
In both implementations, a pointer is maintained that points to the top of the stack, indicating where the next piece of data will be inserted or removed.
---
### **Use Cases for Stacks**
- **Undo functionality** in applications.
- **Backtracking algorithms**, such as navigating back in web browsers.
- **Function call management** in programming languages (call stack).