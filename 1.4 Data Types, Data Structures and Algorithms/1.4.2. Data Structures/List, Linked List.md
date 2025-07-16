Tags: #subnode 

A **linked list** is a dynamic abstract data structure, where each node consists of data and pointer and each node points to the next. Unlike arrays, linked lists do not require contiguous memory locations, allowing for flexible and efficient memory management.

---
### **Structure of a Linked List Node**
- Composed of ‘nodes’
- Each node is composed of two parts
	- The data (which may be a complex data structure)
	- A pointer (the index) of the next node
- A start pointer identifies the first node in the list
- A nextfree pointer shows the index of the next free space in the array

Each **node** in a linked list consists of two fields:
1. **Data Field:** Stores the value of the item.
2. **Pointer Field:** Contains the memory address (pointer) of the next node in the sequence.
For example:
`Index | Data       | Pointer     0   | 'Linked'   | 2     1   | 'Example'  | 0     2   | 'List'     | -`  
- **Start Pointer:** Points to the first node in the list (here, index 1).
- **NextFree Pointer:** Points to the next available space in memory (here, index 3).
- **Null/Empty Pointer:** Signals the end of the list (here, the pointer in index 2).

---
### **Traversal**
When traversing a linked list:
1. Start from the node indicated by the **Start Pointer**.
2. Follow the **Pointer Field** from one node to the next.
3. Stop when you encounter a null pointer.
Example traversal of the above linked list:  
**Output:** `'Example', 'Linked', 'List'`

---
### **Manipulating a Linked List**
#### **Adding a Node**
Adding `'OCR'` after `'Example'` involves:
1. Append `'OCR'` to the list at the **NextFree** index and update `NextFree`:
    `Index | Data      | Pointer     3   | 'OCR'     | -     Start = 1, NextFree = 4`  
2. Update `'Example'`'s pointer to `'OCR'` (index 3):
    `Index | Data      | Pointer     1   | 'Example' | 3`  
3. Update `'OCR'`'s pointer to `'Linked'` (index 0):
    `Index | Data      | Pointer     3   | 'OCR'     | 0`  
4. Traversal now outputs: `'Example', 'OCR', 'Linked', 'List'`.

---
#### **Removing a Node**
Removing `'List'` involves:
1. Update `'Linked'`'s pointer to skip `'List'`:
    `Index | Data      | Pointer     0   | 'Linked'  | -`  
2. Traversal now outputs: `'Example', 'Linked'`.
**Note:** The node is not physically deleted; its pointer is bypassed, leaving it inaccessible and wasting memory.
---
### **Advantages of Linked Lists**
- **Dynamic Size:** Can grow or shrink at runtime.
- **Efficient Insertions/Deletions:** Adjust pointers without shifting elements.
### **Disadvantages of Linked Lists**
- **Extra Memory:** Requires storage for pointers.
- **Sequential Access:** Items must be traversed in order; no direct access like arrays.
- **Memory Waste:** Unused nodes are not removed, leading to inefficient memory use.