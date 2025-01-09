When high-level code is compiled into object code ready for execution, it undergoes four distinct stages: Lexical Analysis, Syntax Analysis, Code Generation, and Optimisation. Each stage plays a crucial role in ensuring the accuracy and efficiency of the final machine code.

---
### **1. Lexical Analysis**
- **Purpose**: The primary function of this stage is to prepare the code for analysis by removing unnecessary elements.
- **Process**:
    - Whitespace and comments are eliminated from the source code.
    - The remaining code is examined to identify keywords, variable names, and constants.
    - These elements are replaced with tokens, which are symbolic representations of the original code components.
- **Symbol Table**:
    - A symbol table is created to store information about each token, such as its type and scope. For example, in the code:
	    `while flag = False:
		    `print "not found";  # terminates when item is found`
- After lexical analysis, it may be simplified to:
	`while flag = False:
	    `print "not found";`
---
### **2. Syntax Analysis**
- **Purpose**: This stage checks the structure of the tokens against the grammatical rules of the programming language.
- **Process**:
    - Tokens are parsed to identify syntax errors (e.g., undeclared variables or mismatched brackets).
    - An **Abstract Syntax Tree (AST)** is generated, representing the hierarchical structure of the source code.
- **Error Detection**:
    - Any syntax errors found are listed for the programmer to correct.
    - **Semantic Analysis** is also performed here to identify logical errors, such as multiple declarations or undeclared identifiers, which might not be strictly syntax-related.
---
### **3. Code Generation**
- **Purpose**: This stage translates the abstract syntax tree into machine code.
- **Process**:
    - The AST is processed to generate corresponding machine code instructions.
    - This machine code is specific to the target processor architecture and is ready for execution.
---
### **4. Optimisation**
- **Purpose**: The goal of this stage is to enhance the efficiency of the generated machine code.
- **Process**:
    - The compiler analyzes the code to find areas where performance can be improved.
    - Insignificant or redundant code is identified and removed.
    - Repeated code sections may be condensed or replaced with more efficient algorithms that yield the same results.
- **Considerations**:
    - While optimisation improves execution speed, excessive optimisation can lead to altered program behavior or unintended consequences.