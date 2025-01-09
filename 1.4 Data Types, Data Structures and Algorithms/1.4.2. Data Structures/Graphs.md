Tags: #subnode 

A **graph** consists of a set of **vertices (nodes)** connected by **edges (arcs)**. Graphs are commonly used in computer science to model networks, relationships, or paths.

---
### **Types of Graphs**
- **Directed Graph:** Edges have a direction and can only be traversed one way.
- **Undirected Graph:** Edges have no direction and can be traversed in either direction.
- **Weighted Graph:** Each edge has a numerical value representing cost, distance, or weight.
---
### **Representing Graphs**
#### **1. Adjacency Matrix**
An adjacency matrix is a 2D array where:
- Rows and columns represent nodes.
- Values indicate the presence (and weight) of edges.  
    If no edge exists, the value is typically `0` or `-`.
Example:
||A|B|C|D|E|
|---|---|---|---|---|---|
|A|-|4|18|12|-|
|B|4|-|5|-|8|
|C|18|5|-|5|-|
|D|12|-|-|-|3|
|E|-|8|-|3|-|

---
#### **2. Adjacency List**
An adjacency list uses a dictionary or linked structure to map each node to its connected nodes and weights.
Example:
`A → {B:4, C:18, D:12}   B → {A:4, C:5, E:8}   C → {A:18, B:5, D:5}   D → {A:12, E:3}   E → {B:8, D:3}`  

---
### **Comparison of Adjacency Matrix and Adjacency List**

|Feature|**Adjacency Matrix**|**Adjacency List**|
|---|---|---|
|**Storage Efficiency**|Requires O(V2)O(V^2)O(V2) space, even for sparse graphs|More space-efficient for sparse graphs|
|**Access Speed**|Faster access (O(1)O(1)O(1)) for edge existence|Slower access (O(k)O(k)O(k)), where kkk is node degree|
|**Addition of Nodes**|Easy to add nodes|More complex; requires updating list|
|**Addition of Edges**|Direct update of matrix cells|Append to lists; efficient for sparse graphs|
|**Best Use Case**|Suitable for dense graphs|Suitable for large, sparse networks|

---
### **Choosing a Representation**
- Use an **adjacency matrix** for dense graphs or when fast edge access is required.
- Use an **adjacency list** for sparse graphs to save memory and maintain scalability.