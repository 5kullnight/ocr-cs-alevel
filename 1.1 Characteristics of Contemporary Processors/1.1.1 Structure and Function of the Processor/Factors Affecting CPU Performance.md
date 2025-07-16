# 1. Clock Speed:
**Definition**: Clock speed refers to how fast the CPU can process instructions. It is determined by the **system clock**, which switches between 0 and 1 to generate pulses. Each CPU operation starts on a clock pulse.
- **Unit**: Measured in **Hertz (Hz)**, typically GHz (billions of cycles per second).
- **Impact**:
	- A higher clock speed means faster processing of instructions.
	- Example: A CPU with a clock speed of **3.2 GHz** completes **3.2 billion cycles per second**.
	- Limitation: Higher speeds can cause overheating, requiring better cooling.
# 2. Number of Cores:
- **Definition**: A core is an independent processing unit within the CPU. Each core can execute its own **fetch-decode-execute cycle** simultaneously.
    - **Impact**:
        - More cores mean the CPU can handle multiple instructions at the same time.
        - Example:
            - A **dual-core** processor can handle **2 tasks** simultaneously.
            - A **quad-core** processor can handle **4 tasks**.
    - **Limitation**: Performance gains depend on software optimization. Some programs are not designed to use multiple cores efficiently.
# 3. Cache Memory:
- **Definition**: Cache memory is a small amount of high-speed memory located inside the CPU. It stores frequently used instructions to improve processing speed.
    - **Impact**:
        - Reduces the time needed to access data from main memory (RAM).
        - Larger or faster cache allows quicker data access.
    - Example: When you use a web browser, it often stores copies of web pages, images, and other resources in a **cache** to improve loading times for frequently visited sites. 
		**How It Works**:
		1. **First Visit**: When you visit a website for the first time, your browser downloads all the necessary files (HTML, CSS, images) from the server and saves them in its cache.
		2. **Subsequent Visits**: On your next visit to the same website, the browser first checks its cache to see if it already has the files needed to display the page. If the files are in the cache, it loads them quickly from local storage instead of downloading them again from the server, resulting in faster loading times.
    - **Types of Cache**:

| Level  | Speed               | Size                     | Location              | Purpose                            |
| ------ | ------------------- | ------------------------ | --------------------- | ---------------------------------- |
| **L1** | Fastest             | Smallest (e.g., 32-64KB) | Inside CPU core       | Stores most critical instructions. |
| **L2** | Slower than L1      | Larger (e.g., 256KB-2MB) | Inside CPU (not core) | Backup for L1.                     |
| **L3** | Slowest (but > RAM) | Largest (e.g., 4-32MB)   | Shared between cores  | Helps with Multi-core Processing.  |
