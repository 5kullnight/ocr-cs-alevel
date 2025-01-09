In computer science, thinking procedurally makes the task of writing a program a lot simpler by breaking a problem down into smaller parts that are easier to understand and consequently easier to design.
The first stage of thinking procedurally in software development involves taking the problem defined by the user and breaking it down into its component parts, in a process called **problem decomposition**. In this process, a large, complex problem is continually broken down into smaller subproblems that can be solved more easily. By separating the problem into sections, it becomes more feasible to manage and can be divided between a group of people according to the skill sets of different individuals.
This process requires software developers to consider a problem in terms of the underlying subproblems that need to be solved to achieve the desired result. An adventure game, for example, might be broken down into the following components:
1. **Characters**
2. **Adventures**
3. **Enemies**
These would then be broken down further, as shown:
1. **Characters**
    - Characters’ interactions
    - Characters’ appearance
2. **Adventures**
    - Levels
    - Backgrounds and settings
3. **Enemies**
    - Enemies’ interactions
    - Enemies’ appearance
Problems are commonly decomposed using **top-down design**, also known as **stepwise refinement**. This is the preferred method used to approach very large problems, as it breaks problems down into levels. Higher levels provide an overview of a problem, while lower levels specify in detail the components of this problem.
The aim of using top-down design is to keep splitting problems into subproblems until each subproblem can be represented as a single task and ideally a self-contained module or subroutine. Each task can then be solved and developed as a subroutine by a different person. Once programmed, subroutines can also be tested separately before being brought together and finally integrated.