Tags: #subnode 

**Definition:**  
A tuple is like a container that holds a group of items in a specific order. Once you create it, you cannot change what’s inside (unlike a list, where you can add, remove, or modify items). Unlike lists, tuples cannot be modified once they are created. They can store elements of different data types and are often used when a collection of values should remain constant.

---
### **Key Characteristics of Tuples**
1. **Immutable:**  
    Once created, elements cannot be added, removed, or altered.  
    Example:
    `tupleExample = ("Value1", 2, "Value3") tupleExample[0] = "NewValue"  # This will raise a SyntaxError`
2. **Ordered:**  
    Elements maintain their order, and you can access them via indexing.
3. **Mixed Data Types:**  
    Tuples can contain elements of various data types.  
    Example: `("Apple", 42, 3.14)`
4. **Initialization:**  
    Tuples are defined using **regular brackets** (`()`), unlike lists which use square brackets (`[]`).  
    Example: `myTuple = (1, "Hello", True)`
---
### **Accessing Tuple Elements**
You can access tuple elements using zero-based indexing, similar to lists and arrays:
`tupleExample = ("Value1", 2, "Value3")   print(tupleExample[0])  # Output: Value1`

---
### **Advantages of Tuples**
1. **Immutability:**  
    Useful for fixed collections of data to prevent accidental modification.
2. **Performance:**  
    Tuples are faster to access and iterate over compared to lists due to their immutability.
3. **Hashable:**  
    Tuples can be used as keys in dictionaries (if they contain only immutable elements).
---
### **Examples**
1. **Creating a Tuple:**
    `myTuple = ("Python", 7, 3.14, False)`
2. **Accessing Elements:**
    `print(myTuple[1])  # Output: 7 print(myTuple[-1])  # Output: False (negative indexing accesses elements from the end)`
3. **Unpacking Tuples:**  
    Tuples can be unpacked into individual variables:
    `a, b, c = (10, 20, 30) print(a)  # Output: 10 print(c)  # Output: 30`
4. **Tuple Length:**  
    Use the `len()` function to find the number of elements in a tuple:
    `print(len(myTuple))  # Output: 4`