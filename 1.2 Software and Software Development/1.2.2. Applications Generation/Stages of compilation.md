When high-level code is compiled into object code ready for execution, it undergoes four distinct stages: Lexical Analysis, Syntax Analysis, Code Generation, and Optimisation. Each stage plays a crucial role in ensuring the accuracy and efficiency of the final machine code.

"Lazy Snakes Can Optimise"
# 1. Lexical Analysis:
- **Lexical** = "Lexicon" = Words. This stage reduces your code to basic vocabulary tokens. Cleans it up like a spellchecker before grammar checking.
- **Purpose**: The primary function of this stage is to prepare the code for analysis by removing unnecessary elements.
- **Process**:
    - Removes whitespace/comments, converts code into tokens, builds symbol table.
    - The remaining code is examined to identify keywords, variable names, and constants.
    - These elements are replaced with tokens, which are symbolic representations of the original code components.
# 2. Syntax Analysis:
- **Think**: Microsoft Word underlining your bad grammar.
- **Purpose**: This stage checks the structure of the tokens against the grammatical rules of the programming language.
- **Process**:
    - Checks tokens against grammar rules, builds AST, detects syntax/semantic errors.
    - An **Abstract Syntax Tree (AST)** is generated, representing the hierarchical structure of the source code.
- **Error Detection**:
    - Any syntax errors found are listed for the programmer to correct.
    - **Semantic Analysis** is also performed here to identify logical errors, such as multiple declarations or undeclared identifiers, which might not be strictly syntax-related.
# 3. Parsing:
- Checks the rules and semantics further, e.g. using stacks that rackets and paired correctly and determines priorities of arithmetic operations.
# 4. Code Generation:
- **Purpose**: This stage translates the abstract syntax tree into machine code.
- **Process**:
    - The AST is processed to generate corresponding machine code instructions.
    - This machine code is specific to the target processor architecture and is ready for execution.
# 5. Optimisation:
- **Purpose**: The goal of this stage is to enhance the efficiency of the generated machine code.
- **Process**:
	- Improves code efficiency by removing redundancies and streamlining logic.
    - The compiler analyzes the code to find areas where performance can be improved.
    - Insignificant or redundant code is identified and removed.
    - Repeated code sections may be condensed or replaced with more efficient algorithms that yield the same results.
- **Considerations**:
    - While optimisation improves execution speed, excessive optimisation can lead to altered program behavior or unintended consequences.

|Stage|Purpose|Key Points|
|---|---|---|
|**Lexical Analysis**|Clean up and tokenise source code|Removes comments/whitespace, creates **tokens**, builds **symbol table**|
|**Syntax Analysis**|Check structure and grammar|Uses **tokens** to build AST, checks for **syntax** and **semantic errors**|
|**Code Generation**|Convert to machine code|AST → Machine code, specific to **CPU architecture**|
|**Optimisation**|Improve efficiency|Removes redundant code, improves speed, but may risk **changing behaviour**|