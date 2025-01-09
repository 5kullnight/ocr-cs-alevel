Tags: #subnode 

A **tree** is a connected graph structure that consists of nodes connected by edges. Each tree has a **root node**, which is the topmost node, and the nodes below it are organized in a hierarchical manner. Trees are fundamental data structures in computer science, used in various applications, including representing hierarchical data, parsing expressions, and implementing search algorithms.

---
### **Key Terminology**
- **Node:** An item or element in the tree.
- **Edge:** A connection between two nodes, also known as a branch or arc.
- **Root:** The top node of the tree, which has no incoming edges.
- **Child:** A node with one or more incoming edges (a node connected to its parent).
- **Parent:** A node that has outgoing edges to its children.
- **Subtree:** A portion of the tree that includes a parent node and all of its descendants.
- **Leaf:** A node that has no children.
---
### **Binary Trees**
A **binary tree** is a specific type of tree where each node can have at most two children, referred to as the left child and the right child. Binary trees are particularly useful for binary search operations because they allow for efficient searching and sorting of data.
#### **Representation of a Binary Tree**
A common way to represent a binary tree is by using a two-dimensional array, where each node is indexed, and pointers indicate the left and right children.

|**Index**|**Left Pointer**|**Data Value**|**Right Pointer**|
|---|---|---|---|
|0|1|G|3|
|1|2|C|4|
|2|-|A|-|
|3|-|J|5|
|4|-|F|-|
|5|-|L|-|

---
### **Tree Traversal Methods**
There are three primary methods for traversing a binary tree:
1. **Pre-order Traversal:**
    - **Order:** Root node, left subtree, right subtree.
    - **Usage:** Used in expressions where the operation precedes the values.
    - **Example Order:** 15, 9, 5, 7, 11, 10, 12, 20, 25, 34
2. **In-order Traversal:**
    - **Order:** Left subtree, root node, right subtree.
    - **Usage:** Useful for obtaining the nodes in sequential order, especially in binary search trees.
    - **Example Order:** 5, 7, 9, 10, 11, 12, 15, 20, 25, 34
3. **Post-order Traversal:**
    - **Order:** Left subtree, right subtree, root node.
    - **Usage:** Useful for deleting or freeing nodes since it processes children before their parents.
    - **Example Order:** 7, 5, 10, 12, 11, 9, 34, 25, 20, 15
---
### **Use Cases for Trees**
- **Hierarchical data representation:** File systems, organizational structures.
- **Searching and sorting:** Binary search trees for efficient data retrieval.
- **Expression parsing:** Representing arithmetic expressions in compilers.