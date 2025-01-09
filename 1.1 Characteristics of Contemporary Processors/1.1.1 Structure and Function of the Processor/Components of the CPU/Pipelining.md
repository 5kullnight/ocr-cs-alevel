- **Definition**: Simultaneous processing of multiple instructions by overlapping steps:
    1. Fetching one instruction.
    2. Decoding another.
    3. Executing a third.
#### **Analogy for Pipelining: Assembly Line in a Factory**
Imagine a factory making cars. Each car goes through multiple stages (steps) to be fully assembled:
1. **Stage 1**: Install the engine.
2. **Stage 2**: Attach the doors.
3. **Stage 3**: Paint the car.
4. **Stage 4**: Final inspection.
---
#### **Non-Pipelined Process (One-at-a-Time)**
- Each car goes through **all stages** before starting the next car.
- Result: Only **one car** is completed at a time.
- Efficiency: Slow, as workers at some stages wait for the previous car to finish.
#### **Stages in Pipelining for a Webpage**
1. **Fetch**: The CPU retrieves the instructions (e.g., "Download HTML, CSS, images") from memory.
2. **Decode**: The CPU decodes each instruction to determine what it needs to do (e.g., "Parse HTML structure").
3. **Execute**: The CPU executes the instruction (e.g., "Render a section of the page").
4. **Write Back**: The CPU stores results or sends them to other components (e.g., "Display rendered content on the screen").

- **Purpose**: Reduces CPU idle time, improves efficiency.
- **Types of Pipelining**:
    - **Instruction Pipelining**: Divides instruction processing into fetch, decode, execute.
    - **Arithmetic Pipelining**: Overlaps arithmetic operation steps.
