Tags: #subnode 

**Definition:**  
A record is a structured data type used to group related fields (attributes) together.  
In databases, a record corresponds to a row, and fields correspond to columns.
**Example:**  
Imagine a table of fighters:

|ID|FirstName|Surname|
|---|---|---|
|001|Antony|Joshua|
|002|Tyson|Fury|
|003|Deontay|Wilder|

Here, each row is a record, and `ID`, `FirstName`, and `Surname` are the fields.

---
### **Declaring a Record Type**
To define a record, use the following syntax:
`fighterDataType = record     integer ID     string FirstName     string Surname   end record`
This creates a template for fighter data with three fields: `ID`, `FirstName`, and `Surname`.

---
### **Creating and Accessing Records**
1. **Create a Record:**  
    Declare a variable using the record type:
    `fighter : fighterDataType`
2. **Accessing Fields:**  
    Use the syntax `recordName.fieldName` to access or modify a field. For example:
    `fighter.FirstName = "Antony"   fighter.Surname = "Joshua"   fighter.ID = 1`
3. **Using a Record:**  
    After filling in the fields, you can process or display the data. For example:
    `print("Fighter's Name: " + fighter.FirstName + " " + fighter.Surname)`  

---
### **Key Points to Remember**
1. **Structure:**  
    A record groups data logically, making it easier to handle complex datasets.
2. **Field Access:**  
    Each field is accessed using its name, ensuring clarity in code.
3. **Real-World Use:**  
    Records are the foundation of database rows and are essential for organizing tabular data.