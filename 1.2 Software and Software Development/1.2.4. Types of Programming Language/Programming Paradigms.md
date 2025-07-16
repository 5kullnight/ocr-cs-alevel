Programming paradigms are frameworks or styles for writing and organizing code to solve problems. They are primarily divided into **imperative** and **declarative** paradigms, each with distinct characteristics and use cases.
# 1. Imperative Paradigm:
Imperative programming defines _how_ a task should be performed through a sequence of commands.
### Procedural Programming:
- **Overview**: A type of imperative programming that structures code into procedures or functions, executed sequentially.
- **Key Features**:
    - Step-by-step instructions.
    - Easy to learn and interpret.
    - Flexible and widely applicable.
- **Examples of Languages**: Pascal, Python, Logo.
- **Use Cases**: General-purpose tasks, educational programming, and structured problem-solving.
### Object-Oriented Programming (OOP):
- **Overview**: Focuses on representing real-world entities as objects formed from classes. Each object contains:
    - **Attributes** (data)
    - **Methods** (functions)
- **Key Features**:
    - Reusability through inheritance.
    - Encapsulation and abstraction to hide implementation details.
    - Polymorphism to adapt methods for different object types.
- **Examples of Languages**: Python, Delphi, Java.
- **Use Cases**: Systems with reusable components, like GUIs, simulations, and games.
# 2. Declarative Paradigm
Declarative programming specifies _what_ the desired outcome is, leaving the _how_ to the programming language.
#### Functional Programming:
- **Overview**: Based on mathematical concepts, focusing on functions and immutability.
- **Key Features**:
    - Avoids changing state or mutable data.
    - Encourages function reuse.
    - Facilitates parallel processing.
- **Examples of Languages**: Haskell, C#, Java.
- **Use Cases**: Data transformation, algorithm design, and parallel computation.
### Logic Programming:
- **Overview**: Defines a problem through facts and rules, allowing queries to derive solutions.
- **Key Features**:
    - Relies on symbolic logic.
    - Abstracts away implementation details.
    - Ideal for knowledge-based systems.
- **Examples of Languages**: Prolog.
- **Use Cases**: Expert systems, AI, and database querying.
### Comparison of Paradigms:

|**Paradigm**|**Characteristics**|**Key Strengths**|**Key Weaknesses**|**Example Problems**|
|---|---|---|---|---|
|**Procedural**|Step-by-step instructions.|Easy to write and debug.|Not scalable for large problems.|Automating repetitive tasks, small applications.|
|**OOP**|Objects with attributes and methods.|Reusable and maintainable.|Can become complex.|GUI development, simulations, games.|
|**Functional**|Stateless and immutable.|Parallel-friendly, concise.|Steep learning curve for beginners.|Data processing, algorithmic transformations.|
|**Logic**|Rules and queries for problem-solving.|Handles AI tasks well.|Limited to specific problems.|Expert systems, AI, and rule-based reasoning.|