---
id: 2l9Pyq2juMt9iXnUJxuE9
title: Processes
desc: ''
updated: 1642291094200
created: 1642291081569
---
# Processes

A process encapsulates the basic resources of memory and processor time. It also encapsulates other higher level resources. Each process:

* has an address space and has some amount of allocated memory.
* consists of one or more threads that are given processor timem, including thread sychronization.
* higher level resources such as open file descriptors.

## Creation of a new process

The operating system usually provides a way to create processes. in UNIX the `fork` system call is used to **duplicate** the callers address space, creating a new address space for a new process.

### Copy on write

When a new process is created via `fork`, the address space is copied. The new process code is identical and is usually read-only so that it can be shared in real memory and no actual copying of memory is required. This is fater and more efficient than making a copy. Copy on write is a technique that makes a copy of a memory region only when the new process actually writes to it.

## New processes on distributed systems

In a distributed system there is a choice as to where the new process will be created on. In a distributed operating system, this choice is made by the operating system. The decision is largely a matter of policy and some categories are:

* **transfer policy :** determines whether the new process is allocated locally or remotely. 
* **location policy :** determines which host, from a set of given hosts, the new process should be allocated on.

  The policy is often transparent to the user and will attempt to take into account such things as relative load across hosts, IPC, architectures and specialised resources that processes may require.

## Process migration

Processes can be migrated from one host to another by copying their address space. Depending on the platform and on the resources that are in current use by the process, process migration can be more or less difficult. Process code is often CPU dependant, this obviously introduces heterogenity issues.
