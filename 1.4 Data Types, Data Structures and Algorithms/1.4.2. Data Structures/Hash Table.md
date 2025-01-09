Tags: #subnode 

A **hash table** is a data structure that pairs keys with values, allowing for fast data retrieval. It uses an array and a **hash function** to map keys to specific indices in the table, enabling efficient access to stored data.

---
### **Key Components of Hash Tables**
1. **Hash Function:**
    - A mathematical function that takes a key (input) and produces an integer (hash) that corresponds to an index in the hash table.
    - A good hash function distributes keys uniformly across the table to minimize collisions.
2. **Keys and Values:**
    - **Key:** A unique identifier used to access the corresponding value in the hash table.
    - **Value:** The data associated with a key.
3. **Collision:**
    - Occurs when two different keys produce the same hash value, leading them to be mapped to the same index in the hash table.
    - Collisions are managed using techniques like **collision resolution**.
---
### **Collision Resolution Techniques**
When a collision occurs, the hash table must handle it to ensure that all values can be stored and accessed correctly. Some common collision resolution methods include:
1. **Chaining:**
    - Each index in the hash table contains a list (or linked list) of entries that map to the same index.
    - When a collision occurs, the new entry is added to the list at that index.
2. **Open Addressing:**
    - When a collision occurs, the hash table searches for the next available index according to a probing sequence (e.g., linear probing, quadratic probing).
    - If the desired index is occupied, the algorithm checks the next index in the sequence until an empty spot is found.
---
### **Advantages of Hash Tables**
- **Fast Access:** Hash tables provide average-case constant time complexity (O(1)) for search, insert, and delete operations due to direct indexing.
- **Efficient Memory Usage:** By storing data in an array with a hash function, hash tables can efficiently manage memory and avoid wasted space.
---
### **Use Cases for Hash Tables**
- **Database Indexing:** Fast lookups of records by unique keys.
- **Caching:** Storing results of expensive computations to speed up subsequent requests.
- **Associative Arrays:** Implementing dictionaries or maps that associate keys with values.