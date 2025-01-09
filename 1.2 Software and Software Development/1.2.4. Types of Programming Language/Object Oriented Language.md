Object-Oriented Programming (OOP) is a paradigm based on the concept of **objects**, which combine **state** (data) and **behavior** (functions or methods). This approach offers a modular structure that simplifies software development and maintenance.

---
### **Key Concepts in OOP**
#### 1. **Class**
- A **class** is a blueprint or template for creating objects.
- It defines:
    - **Attributes**: Properties that describe the state of an object.
    - **Methods**: Functions that define the behavior of an object.
Example:
```
class Library:
    def __init__(self, books, computers):
        self.number_of_books = books
        self.number_of_computers = computers

    def add_book(self):
        self.number_of_books += 1

    def remove_book(self):
        self.number_of_books -= 1
```
---
#### 2. **Object**
- An **object** is an instance of a class, created through a process called **instantiation**.
- Objects share the structure and behavior defined in their class.
Example:
```
library1 = Library(1000, 20)  # Create an object of Library class
library1.add_book()  # Increases the book count
```
---
#### 3. **Encapsulation**
- Encapsulation restricts direct access to an object’s attributes.
- Attributes are declared as **private**, and **getters** and **setters** are used to access or modify them.
Example:
```
class Book:
    def __init__(self, title, author):
        self.__title = title  # Private attribute
        self.__author = author

    def get_title(self):
        return self.__title

    def set_title(self, new_title):
        self.__title = new_title

```
---
#### 4. **Inheritance**
- A **subclass** (child class) inherits the attributes and methods of a **superclass** (parent class).
- This promotes code reuse and modularity.
Example:
```
class Biography(Book):
    def __init__(self, title, author, subject):
        super().__init__(title, author)
        self.subject = subject

```
---
#### 5. **Polymorphism**
- Objects of different classes can be treated as instances of the same superclass but behave differently.
- **Overriding**: Redefining a method in a subclass.
- **Overloading**: Methods with the same name but different parameter lists.
Example (Overriding):
```
class Book:
    def info(self):
        return "This is a book."

class Biography(Book):
    def info(self):
        return "This is a biography."
```
---
### **Advantages of OOP**
1. **Reusability**:
    - Classes can be reused across multiple projects.
    - Inheritance and polymorphism reduce redundancy.
2. **Encapsulation**:
    - Protects data from unintended modifications.
3. **Modularity**:
    - Code is organized into separate, manageable components.
4. **Ease of Maintenance**:
    - Modular design makes updates straightforward.
5. **High Abstraction**:
    - Programmers focus on higher-level logic rather than implementation details.
---
### **Disadvantages of OOP**
1. **Steep Learning Curve**:
    - Requires a different mindset for programmers used to procedural paradigms.
2. **Overhead**:
    - Increased complexity for small or simple problems.
3. **Design-Intensive**:
    - Requires detailed planning before implementation.
---
### **Example: Pseudocode for Book Class**
```
class Book:
    private reserved
    private onLoan
    private author
    private title

    public procedure new(title, author, reserved, onLoan):
        self.title = title
        self.author = author
        self.reserved = reserved
        self.onLoan = onLoan

    public function set_reserved():
        self.reserved = True

```
Creating and modifying an object:
```
myBook = Book('Great Expectations', 'Charles Dickens', False, False)
myBook.set_reserved()
```
