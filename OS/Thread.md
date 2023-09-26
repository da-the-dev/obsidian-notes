*In* traditional OSs each [[Process|process]] has its own **single node of control**.
Threads are "miniprocesses".

Sometimes, we need many threads of control in the same address space, running "parallel", as if they were separate processes.

Each thread has its own stack

# Reasons to split into threads
- Decomposing large apps into subproceses
- Parallel I/O
## Example
A three-threaded word processor. If a sentence is deleted, first thread reformats the document, while the second one is ready to accept keyboard input. The third thread saves the document onto the disk. 
Three separate processes would not work, because only threads can work on one document. Threads can have shared memory.
![[Pasted image 20230913223529.png]]
