A process is an instance of an executing program including the current values of the program counter, register, and values.
All runnable software is organized into processes.
Each process has is own virtual [[CPU]]. In reality, CPU switches between processes.
Since only one process can be run on 1 CPU, once CPU wants to switch to a different process, current program counter is moved from the PC register to a corresponding place in memory. This process is called [[Multiprogramming|multiprogramming]].

# Process creation
1. System initialization
2. Execution of a process creation system call by a running process
3. A user request to create a new process
4. Initiation of a batch job
## Forking
Process is created as **fork** of a system process. Forking makes an exact copy of a system process. The forked process has the same memory image, environment string and open files as the parent process. After forking, the child process calls `execve` (or similar) to complete the redirection and change the memory image.
# Process termination
- Normal exit (voluntary)
- Error exit (voluntary)
- Fatal exit (Crash) (involuntary )
- Killed by another process (involuntary)
# Process states
- Running (actually using the [[CPU]] right now)
- Ready (ready to run, stopped)
- Blocked (cannot be run, unless something happens, input for example)
![[Pasted image 20230913204552.png]]
### More in-depth on process states
- The process is executing in user mode
- The process is executing in kernel mode
- The process is not executing but is ready to run as soon as the kernel schedules it
- The process is sleeping and resides in main memory
- The process is ready to run, but the swapper (process 0) must swap the process into main memory before the kernel can schedule it to execute
- A process is **preempted** if it was supposed to be scheduled to run, but the scheduler decided to reschedule for another process. Then the first process is preemted.
![[Pasted image 20230913210342.png]]

# Implementation
The OS maintains a process table, one entry per process.
The entry contains info on the process, namely:
- current PC
- stack pointer
- memory allocation
- status of opened files
- accounting and scheduling info
- etc.

