---
id: PaxNSXAFwbSxEtEbYKzoj
title: Distributed Systems
desc: ''
updated: 1642294462078
created: 1642228084230
---

# Distributed Systems

## What is a distributed system?

* A system in which hardware or software components located at networked computers communicate and coordinate their efforts
* A collection of independant computers that appears to its users as a single computer.

### Key Aspects

* a number of components
* communication between components
* achieve more than the simple sum of individual components

## Computer Networks vs Distributed Systems

**Computer Network** : Is a collection of spatially seperated, interconnected computer that exchange messages based on specific protocols. Computers are addressed by IP addresses.

**Distributed System :** Multiple computers on the network working together as a system. The spatial seperation of computers and communication aspects are hidden from users.

## Why Distributed Systems?

### Resource sharing

* Hardware
* Software
* Other \(Processing power, memory, bandwidth\)

### Benefits of resource sharing

* Economy
* Reliability
* Availability
* Scalability

## Consequences of Distributed Systems

* Concurrency : In a distributed system computers perform their tasks autonomously and communicate with other computers. Services provided by distributed systems will be accessed by multiple users. Distributed systems should take this into consideration.
* No global clock : Clocks on individual computers operate independantly. There are limits to the accuracy with which computers in the system can synchronize their clocks.
* Independant failures : Some components may fail while others are running. Failures of participating computers of the system is not known to others immediately.

