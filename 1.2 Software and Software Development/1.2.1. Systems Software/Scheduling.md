Scheduling is a fundamental function of the operating system, ensuring that all running programs receive fair and efficient access to the CPU. By implementing various scheduling algorithms, the operating system can manage processor time effectively. Scheduling algorithms can be categorized into two types:
1. **Preemptive Scheduling**: The operating system can interrupt jobs, allowing it to allocate processor time dynamically.
    - **Examples**:
        - Multilevel Feedback Queues
        - Shortest Remaining Time
        - Round Robin
2. **Non-Preemptive Scheduling**: Once a job starts executing, it runs to completion without being interrupted.
    - **Examples**:
        - First Come First Served
        - Shortest Job First
# Key Scheduling Algorithms:

"Massive Sandwiches Rarely Stay For-long!"
### 1. Multilevel Feedback Queues:
- **Description**: Utilizes multiple queues, each with different priority levels. Jobs can move between queues based on their execution characteristics (e.g., how long they’ve been waiting or how much CPU time they’ve consumed).
- **Advantages**: Can adapt to changing workloads and prioritize important tasks more effectively.
- **Disadvantages**: Complexity in implementation and decision-making for prioritization can be challenging.
### 2. Shortest Job First (SJF):
- **Description**: Jobs are queued based on their expected execution time, with the shortest jobs being executed first.
- **Advantages**: Minimizes the average waiting time for a group of jobs.
- **Disadvantages**: Requires knowledge of job durations in advance, which can be difficult to predict. Risk of processor starvation if short jobs are continuously added.
### 3. Round Robin (RR):
- **Description**: Each job receives a fixed time slice during which it can execute. After a job's time slice expires, it is moved to the back of the queue, and the next job in line gets its time slice. This process continues until all jobs are completed.
- **Advantages**: Fair allocation of CPU time to all jobs. Allow multi-tasking to take place. To limit each process to a certain amount of time. So OS cycles through all processes fairly.
- **Disadvantages**: Longer jobs can take significantly longer to complete since they are divided into smaller time slices. Does not prioritize jobs based on urgency or importance.
### 4. Shortest Remaining Time (SRT):
- **Description**: A Interruptible version of SJF, where the job with the least time left for completion is executed first. If a new job arrives with a shorter remaining time than the currently running job, the CPU will switch to the new job.
- **Advantages**: Provides quick responses for short tasks.
- **Disadvantages**: Similar to SJF, it can lead to processor starvation for longer jobs.
### 5. First Come First Served (FCFS):
- **Description**: Jobs are processed in the order they arrive in the queue, with the first job being executed first.
- **Advantages**: Simple and easy to implement.
- **Disadvantages**: Does not prioritize jobs; longer jobs can delay shorter ones, leading to increased average waiting time.

| Scheduler | Preemptive | Fairness  | Starvation Risk | Notes                             |
| --------- | ---------- | --------- | --------------- | --------------------------------- |
| MFBQ      | ✅          | Very High | Low             | Very dynamic & adaptable          |
| SJF       | ❌          | Low       | Very High       | Efficient but unfair              |
| RR        | ✅          | High      | Low             | Good for time-sharing systems     |
| SRTF      | ✅          | Medium    | High            | Best turnaround time              |
| FCFS      | ❌          | Low       | High            | Very basic, poor for multitasking |
**Preemptive scheduling** = the CPU **can interrupt a running process** to give time to a different process.