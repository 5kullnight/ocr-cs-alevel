Tags: #subnode 

A **queue** is a data structure that operates on a First In, First Out (FIFO) basis, meaning the first item added to the queue is the first one to be removed. Queues are widely used in various applications, such as managing tasks in printers, handling keyboard inputs, and simulating scenarios where order matters.

---
### **Types of Queues**
1. **Linear Queue:**
    - Consists of an array where items are added to the end and removed from the front.
    - Utilizes two pointers: one pointing to the front and another to the back.
    - As items are removed, addresses in the array become unusable, making this implementation less efficient.
2. **Circular Queue:**
    - Similar to a linear queue but designed to reuse empty spaces in the array.
    - When the rear pointer reaches the maximum size of the queue, it loops back to the front of the array, allowing new items to be added in available spaces.
    - More efficient in space utilization but harder to implement.
---
### **Queue Operations**
The following operations can be performed on a queue:

|**Operation**|**Syntax**|**Description**|**Example Output**|
|---|---|---|---|
|**enQueue(value)**|`Queue.enQueue("Nadia")`|Adds a new item to the end of the queue. Increments the back pointer.||
||`Queue.enQueue("Elijah")`|||
|**deQueue()**|`Queue.deQueue()`|Removes the item from the front of the queue. Increments the front pointer.||
|**isEmpty()**|`Queue.isEmpty()`|Checks if the queue is empty by comparing the front and back pointers.|`False`|
|**isFull()**|`Queue.isFull()`|Checks if the queue is full by comparing the back pointer and queue size.|`False`|

---
### **Example of Linear Queue Manipulation**
- **Adding Items (enQueue):**
    - `enQueue(Task3)`
    - Queue: `[Task1, Task2, Task3]`
- **Removing Items (deQueue):**
    - `deQueue()`
    - Queue after removal: `[Task2, Task3]`
- **Adding Another Item:**
    - `enQueue(Task4)`
    - Queue: `[Task2, Task3, Task4]`
- **Removing Another Item:**
    - `deQueue()`
    - Queue after removal: `[Task3, Task4]`
---
### **Example of Circular Queue Manipulation**
- **Adding Items:**
    - `enQueue(Task5)` → Queue: `[Task3, Task4, Task5]` (rearPointer: 4)
    - `enQueue(Task6)` → Queue: `[Task3, Task4, Task5, Task6]` (rearPointer: 5)
    - `enQueue(Task7)` → Queue: `[Task7, Task3, Task4, Task5, Task6]` (rearPointer: 0, wrapping around)
---
### **Use Cases for Queues**
- **Task scheduling** in operating systems.
- **Buffer management** for data streams, such as keyboard inputs.
- **Handling requests** in web servers.
### Similarities & differences:
| **Aspect**                 | Similiraties                                                                 |     |
| -------------------------- | ---------------------------------------------------------------------------- | --- |
| **Linear data structures** | Both are linear data structures that store data in a sequence.               |     |
| **Dynamic or static**      | Both can be implemented using arrays (static) or linked lists (dynamic).     |     |
| **Access is restricted**   | You can only insert/remove from specific ends (not randomly like in arrays). |     |
| **Used in algorithms**     | Both are used widely in various algorithms and real-life computing tasks.    |     |
| **Pointer-based access**   | Both use pointers (or indices) to track position of elements.                |     |

|**Aspect**|**Stack** (LIFO)|**Queue** (FIFO)|
|---|---|---|
|**Access Order**|Last In, First Out (LIFO) – last item added is removed first|First In, First Out (FIFO) – first item added is removed first|
|**Insertion Point**|Elements are added at the **top**|Elements are added at the **rear (end)**|
|**Removal Point**|Elements are removed from the **top**|Elements are removed from the **front**|
|**Number of Pointers**|Usually uses **one pointer** (top)|Uses **two pointers** (front and rear)|
|**Use Cases**|Function calls, undo features, backtracking|Task scheduling, queues in OS or networks|
|**Complexity**|Easier to implement|Slightly more complex, especially circular queues|