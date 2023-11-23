# XV Quiz (CSL 3030)

Welcome to the XV Quiz for CSL 3030 - Operating Systems!



## Instructions
- Answer the multiple-choice questions by selecting the correct option.
- For theoretical questions, provide concise and accurate explanations.
- Feel free to use this quiz for self-assessment or educational purposes.

## Multiple-Choice Questions

#### Question 1: Basics
1. What is XV6?
   - a. A programming language
   - b. A Unix-like operating system
   - c. A file system
   - d. An assembly language

#### Question 2: Architecture
2. XV6 is based on which earlier operating system?
   - a. Windows
   - b. Linux
   - c. BSD
   - d. DOS

#### Question 3: File System
3. Which file system is used in XV6?
   - a. FAT32
   - b. NTFS
   - c. ext4
   - d. simple

#### Question 4: System Calls
4. How are system calls implemented in XV6?
   - a. As functions in the C standard library
   - b. As interrupts
   - c. Through the command line
   - d. As external programs

#### Question 5: Processes
5. In XV6, what is the maximum number of processes that can run simultaneously?
   - a. 128
   - b. 256
   - c. 512
   - d. 1024

#### Question 6: Shell
6. What is the name of the shell used in XV6?
   - a. Bash
   - b. Zsh
   - c. Sh
   - d. Fish

#### Question 7: Scheduling
7. How does XV6 handle process scheduling?
   - a. Round-robin scheduling
   - b. Priority-based scheduling
   - c. First-Come-First-Serve (FCFS)
   - d. Random scheduling

#### Question 8: Memory Management
8. Which memory management technique is used in XV6?
   - a. Paging
   - b. Segmentation
   - c. Virtual Memory
   - d. None of the above

#### Question 9: Interrupts
9. How are interrupts handled in XV6?
   - a. Through polling
   - b. Using hardware interrupts
   - c. Using software interrupts
   - d. Both b and c

#### Question 10: Multithreading
10. Does XV6 support multithreading?
    - a. Yes
    - b. No

#### Bonus Question:
11. Who developed XV6?
    - a. Microsoft
    - b. Google
    - c. MIT
    - d. IBM

## Theoretical Questions

#### Question 12: Process States
12. Briefly explain the different states a process can be in within the XV6 operating system.

#### Question 13: File System Structure
13. Describe the structure of the file system in XV6. Include the key components and their roles.

#### Question 14: System Calls vs. Library Functions
14. Explain the difference between system calls and library functions in the context of XV6. Provide examples of each.

#### Question 15: Memory Paging
15. How does memory paging work in XV6? Discuss the benefits of using paging in memory management.

#### Question 16: Shell Commands
16. Name and briefly explain three essential shell commands in the XV6 operating system.

#### Question 17: Process Synchronization
17. Discuss the concept of process synchronization in XV6. Why is it essential, and what mechanisms are used to achieve it?

#### Question 18: Interrupt Handling
18. Explain the role of interrupts in the XV6 operating system. How are interrupts handled, and what is their significance in system operation?

#### Question 19: Virtual Memory
19. What is virtual memory, and how is it implemented in XV6? Discuss the advantages of using virtual memory.

#### Question 20: Boot Process
20. Outline the steps involved in the boot process of XV6. What happens from the moment the computer is powered on to when the XV6 kernel is loaded into memory?

## Answers
Please write your answers here
1. b
2. c
3. d
4. b
5. a
6. c
7. a
8. a
9. d
10. b
11. c
12. The different process states in XV6 are:
- Unused - The process slot/table entry is unused
- Embryo - The process has been allocated a slot but has not been fully initialized yet 
- Sleeping - The process is not runnable, it is waiting for some event
- Runnable - The process is ready to run but not currently running
- Running - The process is currently executed on the CPU
- Zombie - The process has finished execution but still has an entry for the parent to access

13. The XV6 file system structure consists of:
- Superblock - Contains metadata like size of file system, number of data blocks, etc.
- Inode blocks - An inode represents a file and contains metadata like size, permissions, data block addresses, etc. 
- Data blocks - Contain the actual file content
- Directories - Keep track of free/allocated inodes and data blocks

14. System calls are APIs for programs to request services from the kernel. example fork. Library functions are APIs that run in user space, like printf. The key difference is that library functions don't require privileged operations so they can run in user space, while system calls require kernel privileges.

15. Memory paging in XV6 involves breaking physical memory into fixed sized pages for efficient memory usage

16. Some essential XV6 shell commands are:
- ls - List files and directories
- cd - change directory
- sh - Run the shell

17. Mechanisms like locks and semaphores are used to coordinate acces to shared resources, preventing conflict

18. events that  alter natural program flow. The kernel handles interrupts by invoking corresponding ISR's

19. uses paging to allow process to have illusion of larger memory

20. The XV6 boot process begins when the computer is powered on and the CPU starts executing bootloader code in ROM. This loads the kernel image into memory and sets up page tables and segment descriptors. It then transfers control to higher kernel code which initializes device drivers and subsystems. Finally, main() starts initializing processes, buffers, files, inodes and calls userinit() to spawn the first process which executes the shell /initcode/sh command.
