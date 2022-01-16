---
id: 2ZqxKm4UQfYe7paOcGEmm
title: Memory
desc: ''
updated: 1642291009103
created: 1642290980215
---
# Memory

## Address Space

Most operating systems allocate a virtual address space for each process. The virtual addresss space is byte addressable and on a 32 bit computer has 2^32 byte addresses.

The virtual address space can be divided into regions that are **contigous and do not have overlap.**

A paged virtual memory scheme divides the address space into fixed sized blocks that are either located in physical memory \(RAM\) or located in swap space on the hard disk drive.

A page table is used by the processor and operating system to map virtual addresses to real addresses. The page table also contains access control bits for each page that determine, among other things the access privelages of the process on a per page basis.

## Shared memory

Two seperate address spaces can share the same real memory. This can be useful in a number of ways:

* Libraries: The binary code for a library can be large and is the same for all the processes that use it. 
* Kernel: The kernel maintains code and data that is often identical \(system calls for example\).
* Data sharing and communication: Two processes may opt to communicate this way, given a kernel allows for such functionality.
