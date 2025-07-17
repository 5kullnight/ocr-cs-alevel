At its core, abstraction allows non-experts to make use of a range of systems or models by hiding information that is too complex or irrelevant to the system’s purpose. Abstraction enables more efficient design during software development, as programmers can focus on elements that need to be built into the software rather than worrying about unnecessary details. This reduces the time spent on the project. Removing wasteful details early on also prevents the program from becoming unnecessarily large.

---
# Layers of Abstraction in Programming Languages
Layers of abstraction are used within networking and programming languages. Programming languages can be separated into a spectrum of high and low-level languages:
## Low-Level Languages
- Low-level languages, such as assembly code and machine code, directly interact with computer systems but are more difficult to write.
- Programming using machine code requires an understanding of the functions specific binary codes perform.
- Although assembly code is easier to memorise, it still requires programmers to know the mnemonics associated with the instruction set specific to the processor.
---
## High-Level Languages
- High-level languages provide an abstraction for the machine code that is executed when a program is run.
- This makes the process of developing programs easier, as the syntax in high-level languages parallels natural language and is considerably easier to learn and use compared to low-level languages.
- This accessibility has made coding available to non-specialists.
---
# The TCP/IP Model
The TCP/IP model is an abstraction for how networks function, separated into four layers of abstraction: application, transport, internet, and link. Each layer deals with a different part of the communication process, and separating these stages makes them simpler to understand. Each layer does not need to know how other layers work.
- Outgoing communication is visualised as going down these layers, while incoming information can be imagined as going up these layers.
- However, it is important to ensure compatibility between these layers, so standards must be agreed upon in advance.
- The TCP/IP model uses a set of protocols, which means that each layer can be dealt with individually, with details about other layers being hidden.