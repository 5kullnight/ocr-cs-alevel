Tags: #subnode 

**Definition:**  
A list is a data structure used to store an ordered collection of elements. Unlike arrays, lists can store elements of different data types, and their elements are stored non-contiguously in memory.

---
### **Key Features of Lists**
1. **Duplicate Items:**  
    Lists can contain repeated elements.  
    Example: `myList = [23, 36, 62, 23]`
2. **Mixed Data Types:**  
    Lists can hold elements of various data types (e.g., integers, strings, floats).  
    Example: `mixedList = [42, "Hello", 3.14]`
3. **Dynamic Length:**  
    Lists can grow or shrink dynamically by adding or removing elements.
---
### **Accessing Elements**
Elements are accessed using zero-based indexing:
`List = [23, 36, 62, 49]   print(List[1])  # Output: 36`  

---
### **Manipulating Lists**

|**Operation**|**Example**|**Description**|
|---|---|---|
|**isEmpty()**|`List.isEmpty()`|Checks if the list is empty. Returns `True` or `False`.|
|**append(value)**|`List.append(15)`|Adds a new value to the end of the list.|
|**remove(value)**|`List.remove(23)`|Removes the first occurrence of the specified value.|
|**search(value)**|`List.search(38)`|Searches for a value in the list. Returns `True` if found, otherwise `False`.|
|**length()**|`List.length()`|Returns the number of elements in the list.|
|**index(value)**|`List.index(23)`|Returns the position of the first occurrence of the specified value.|
|**insert(position, value)**|`List.insert(4, 25)`|Inserts a value at a specified position in the list.|
|**pop()**|`List.pop()`|Removes and returns the last value in the list.|
|**pop(position)**|`List.pop(3)`|Removes and returns the value at a specified position in the list.|

---

### **Examples**
1. **Appending and Removing Values:**
    `List = [23, 36, 62, 49]   List.append(15)   print(List)  # Output: [23, 36, 62, 49, 15]    List.remove(36)   print(List)  # Output: [23, 62, 49, 15]`
2. **Searching and Indexing:**
    `List = [23, 36, 62, 49]   print(List.search(62))  # Output: True   print(List.index(49))   # Output: 3`
3. **Inserting and Popping Elements:**
    `List = [23, 36, 62, 49]   List.insert(2, 88)   print(List)  # Output: [23, 36, 88, 62, 49]    value = List.pop()   print(value)  # Output: 49   print(List)   # Output: [23, 36, 88, 62]`