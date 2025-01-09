- **Definition**: Parallel wires connecting CPU components; grouped as the **system bus**.
- **Bus Width**: Number of wires; determines bits transferable at once (e.g., 8, 16, 32, 64 bits).
	  - 8 bit Gaming Consoles: Nintendo Entertainment System (NES).
	  - 16 bit Gaming Consoles: Super Nintendo Entertainment System (SNES). Sega Genesis.
	  - 32 bit Gaming Consoles: Nintendo 64 (despite its name, much of the system's data paths were 32-bit); Operating Systems: Windows XP and earlier 32-bit OS versions.
	  - 64 bit Modern Computers: All modern desktops and laptops; Gaming Consoles: PlayStation 4, Xbox One, and later consoles.
- **Example:**
	- Buses in a CPU are like **highways** that allow information to travel between different parts of the computer. There are three main types of buses, each serving a specific purpose: **Data Bus**, **Address Bus**, and **Control Bus**.
#### Types of Buses:
1. **Data Bus**:
	- **Purpose**: Transfers actual data between the CPU, memory, and other devices.
	- **Direction**: **Bi-directional** (data can flow both ways).
	- **In IRL Example:** Postman Delivering Letters
		- Imagine the data bus as a postman delivering letters:
	    - When you write a letter, the postman takes it from your house (CPU) and delivers it to someone else (memory).
	    - Similarly, the postman can bring letters from others to you.
	- **In a CPU Example**:
		- Suppose the CPU needs to add two numbers stored in memory:
	    1. The CPU uses the **data bus** to fetch the numbers (e.g., **7** and **5**) from memory.
	    2. After the addition, the CPU uses the **data bus** again to send the result (e.g., **12**) back to memory.
2. **Address Bus**: 
	- **Purpose**: Transmits the **address** of the location in memory where data is stored or needs to be sent.
	- **Direction**: **Uni-directional** (from CPU to memory or I/O devices).
	- **Example: Street Directory**
		- Imagine the address bus as a street directory or GPS:
	    - You tell the postman (data bus) the exact address of the house (memory location) where the letter should go.
	    - The address bus ensures the postman knows where to deliver the letter.
	- **In a CPU Example**:
		- Continuing the example of adding two numbers:
	    1. The CPU uses the **address bus** to point to the memory location where the first number (**7**) is stored.
	    2. The address bus then points to the memory location of the second number (**5**) for retrieval.
3. **Control Bus**: 
    - **Purpose**: Sends control signals to manage how the CPU and other components communicate.
	- **Direction**: **Bi-directional** (coordinates signals both ways).
	- **Example: Traffic Lights**
		- Imagine the control bus as a set of traffic lights:
	    - It signals when cars (data) should move and when to stop.
	    - It ensures vehicles (data) from different directions don't collide or move at the wrong time.
	- **In a CPU Example**:
		- While adding two numbers:
	    1. The control bus sends a **"read" signal** to memory, instructing it to send the number **7** to the CPU.
	    2. After the CPU processes the addition, the control bus sends a **"write" signal**, telling memory to store the result (**12**).