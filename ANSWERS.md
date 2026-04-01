# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**

A thread is a smaller unit of execution inside a process that shares memory with other threads whereas a process is an independent program with its own memory space Compared to processes threads can be created more quickly and with less weight. Additionally they have the same memory area which facilitates and improves communication We used threads in this assignment because they make managing several tasks easier and allow for speedier execution It would take more time and effort to create distinct procedures Because threads effectively represent concurrent processing  they are more suited for mimicking CPU scheduling.
---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**

[Write your answer here. Describe the specific behavior - where does the process go? When does it run again? Give an example from your actual program output showing a process that was re-queued.]

Example from my output:
```
[P2's quantum execution took 3000 ms, and its quantum completion took 3000 ms. Total advancement: 45%
Time left: 3522 ms
P2 provides the CPU for the context switch.

P2 (Priority: 5) is now in the ready queue. 6522 ms is the burst time.
```

**Explanation of example:**
[Explain what's happening in the output snippet you pasted]

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

Prior to being put to the queue, P1 is in the New state when it is initially generated in the program. After that, it is put in the ready queue and waits for CPU time before becoming Runnable. P1 enters the Running state and starts running inside the run() method when thread.start() is called. When it is executing, it might go into a Waiting-like state when Thread or other processes are active.To mimic execution time, use sleep(). When P1 completes its execution and its remainingTime is 0, it finally enters the Terminated state.
---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**
### First Example: Web Server A web server manages several user requests concurrently, including loading webpages for several users. Why Round-Robin is effective in this situation: Because it allocates a reasonable amount of CPU time to each request, round-robin scheduling is beneficial. This keeps a single request from using every resource. Additionally, it enhances responsiveness to reduce waiting times for users. As a result, the system is more effective and balanced. ---
--- 
### Operating System Task Scheduling The second example Multiple programs, including browsers, games, and background apps, are run simultaneously by an operating system. Why Round-Robin is effective in this situation: Each program can use the CPU for a predetermined amount of time thanks to Round-Robin. This guarantees equity among procedures. Because no application may block another for an extended period of time, it also maintains the system's responsiveness. This is crucial in situations where people are multitasking.
---


## Summary

**Key concepts I understood through these questions:
1. The difference between threads and processes and why threads are more efficient.
2. How Round-Robin scheduling works and how processes are re-added to the ready queue.
3. The lifecycle of a thread and how it moves between different states.

**Concepts I need to study more:
1. Thread synchronization and how to manage shared resources safely.
