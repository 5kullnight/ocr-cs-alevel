Memory management is a crucial function of the operating system that ensures efficient sharing and utilization of computer memory among multiple programs and applications. Given that main memory (RAM) may not be large enough to accommodate all running programs simultaneously, memory management employs techniques such as **paging**, **segmentation**, and **virtual memory** to optimize memory use.
# 1. Paging:
- **Definition**: Paging physically divides main memory into fixed-size frames. Programs are also split into pages of the same size. 
- **Functionality**: When a program is executed, its pages can be loaded into and swapped out of main memory as needed, allowing for better memory allocation without fragmentation (inefficient use of memory that can occur when memory is allocated and deallocated in variable-sized blocks).
![[Pasted image 20250603202702.png]]
# 2. Segmentation:
- **Definition**: Divides memory into **logical segments** of varying sizes, each representing a functional unit of a program (e.g., code, stack, heap, or data structures). Segments are allocated dynamically based on program needs.
- **Functionality**: Segments are allocated based on the program's structure, making it easier to manage and access program components logically. This approach allows for a more intuitive way to manage memory, reflecting the actual usage patterns of the program.
![[Pasted image 20250603202712.png]]
# 3. Virtual Memory:
- **Definition**: Virtual memory extends the available memory by using a portion of the hard disk as if it were RAM. It allows a system to run larger applications than the physical memory could normally support.
- **Functionality**: When RAM is full, sections of programs that are not currently in use are temporarily moved to **virtual memory** through paging, freeing up RAM for active programs. This mechanism improves multitasking capabilities.
### Disk Thrashing:
- **Issue**: A potential problem associated with these memory management techniques is **disk thrashing**.
    - **Definition**: Disk thrashing occurs when the operating system spends more time swapping pages between the hard disk and RAM than executing programs, causing a significant slowdown or freezing of the system.
    - **Cause**: It usually happens when there is insufficient physical memory, leading to excessive paging and frequent access to the hard disk.
### Similarities and Differences Between Paging and Segmentation:

|**Category**|**Aspect**|**Paging**|**Segmentation**|
|---|---|---|---|
|**Similarities**|Purpose|Both are memory management techniques to divide a process into smaller parts.|Both enable programs to use non-contiguous memory efficiently.|
||Address Translation|Both use tables (page table for paging, segment table for segmentation) to map logical to physical addresses.||
||Protection and Sharing|Both can provide mechanisms for memory protection and sharing between processes.||
|**Differences**|Division Basis|Divides memory into fixed-sized blocks (pages), ignoring logical structure.|Divides memory into variable-sized blocks (segments) based on logical structure.|
||Block Size|Pages are of fixed size (e.g., 4 KB, 8 KB).|Segments are of variable size, defined by program structure (e.g., arrays, functions).|
||Fragmentation|Causes **internal fragmentation** due to unused space in pages.|Causes **external fragmentation** due to varying segment sizes.|
||Translation Mechanism|Uses a **page table** to map page numbers to physical frames.|Uses a **segment table** to map segment numbers to physical addresses.|
||Ease of Implementation|Simpler to implement due to uniform page sizes.|More complex to implement due to variable-sized segments.|
||Suitability|Suitable for systems requiring uniform memory block sizes.|Suitable for systems needing logical program divisions.|
