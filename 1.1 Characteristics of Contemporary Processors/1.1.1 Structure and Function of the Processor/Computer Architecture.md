# 1. Von Neumann Architecture:
- **Description**:
    - Uses a **single memory** for both data and instructions e.g. single control unit
    - Data and instructions are transferred along a **shared data bus**.
    - Built on the **stored program concept**, where programs and data are stored in memory.
    - Uses FDE cycle
- **Advantages**:
    - **Cheaper to develop**: The control unit is simpler, reducing costs.
    - **Program optimization**: Programs can be minimized in size.
- **Limitation**:
    - **Bottleneck issue**: Only one data or instruction can travel at a time along the bus, slowing performance.
![[Pasted image 20250603200214.png]]
---
# 2. Harvard Architecture
- **Description**:
    - Uses **separate memory** for data and instructions.
    - Different buses are used for data and instruction transfer, allowing simultaneous access.
    - Often used in **embedded systems** or applications where performance is critical.
- **Advantages**:
    - **Faster execution**: Data and instructions can be fetched in parallel.
    - **Flexible memory sizes**: Instruction memory can be optimized for size and characteristics (e.g., read-only), while data memory can be read-write.
- **Drawbacks:**
	- **Higher Cost**:
	    - The use of separate memory for data and instructions requires more hardware components, making it more expensive to develop and manufacture.
	- **Inefficient Memory Utilization**:
	    - Having dedicated memory for instructions and data can lead to inefficiencies if one type of memory becomes full, while the other has unused space, resulting in wasted resources.
- **Use Case**:
    - Embedded processors in devices like **microwave ovens**, TV remotes, or **medical devices** often use Harvard architecture to maximize efficiency.
![[Pasted image 20250603200228.png]]
---
# 3. Contemporary Processing
- **Hybrid Approach**: Modern CPUs combine elements of both architectures:
    - **Von Neumann**: Used when working with **main memory** to store data and instructions.
    - **Harvard**: Used for **cache memory**, splitting it into:
        - **Instruction cache**: Stores frequently used instructions.
        - **Data cache**: Stores frequently accessed data.
- **Benefits**:
    - Leverages the simplicity of Von Neumann for general tasks.
    - Utilizes the speed of Harvard architecture for cache operations.
- **Drawbacks:**
	- **Increased Complexity**:
	    - The combination of Von Neumann and Harvard architectures complicates design and debugging due to the need for additional circuitry and management of separate caches.
	- **Cache Coherency Issues**:
	    - Maintaining consistency between instruction and data caches can lead to errors if changes in data are not reflected immediately, potentially causing the CPU to execute outdated instructions.
- **Example**:
    - A **smartphone CPU**:
        - Von Neumann architecture handles general apps.
        - Harvard architecture ensures quick access to frequently used functions like camera operations.
---
### Key Differences:

|**Aspect**|**Von Neumann**|**Harvard**|
|---|---|---|
|**Memory**|Shared for data and instructions|Separate for data and instructions|
|**Execution Speed**|Slower (one at a time)|Faster (parallel fetches)|
|**Cost**|Cheaper|More expensive|
|**Use Case**|General-purpose computing|Embedded systems|