---
id: plRmf8Ls6kMFpgcwKSw71
title: Challenges
desc: ''
updated: 1642294562739
created: 1642294507515
---
# Challenges of Distributed Systems

* Heterogenity
* Openness
* Security
* Scalability
* Failure Handling
* Concurrency
* Transparency

## Heterogenity

Distributed Systems may use completely different hardware and software. These listed above are examples of differring hardware/software:

* Networks
* Computer Hardware
* Operating Systems
* Programming Languages
* Implementation by different developers

  These problems have some solutions such as:

* Using standard protocols
* Using agreed upon message formats and data types
* Adhering to an API
* Middleware
* Portable code \(code that is not tighly coupled to specific hardware\)

## Middleware

Middleware is a software layer between the distributed application and the operating system that:

* provides a programming abstraction and
* masks the heterogenity of underlying platform

### Middleware Models

* Distributed File Systems
* Remote Procedure Call \(RPC\)
* Remote Method Invocation \(RMI\)
* Distributed Documents
* Distributed Databases

## Openness

Openness refers to the ability to extend the system in different ways by adding hardware or software resources. Following are some approaches to address openness:

* Publishing key interfaces
* Allowing a uniform communication mechanism to communicate over the published interfaces.
* Ensuring all implementations adhere to the published standards.

## Security

There are three aspects of security:

1. Confidentiality
2. Integrity
3. Availability

Security Mechanisms:

1. Encryption
2. Authentication
3. Authorization

## Scalability

A system should be able to handle growth in users.

### Scalability Challenges

* Cost of physical resources
* Controlling performance loss
* Resources should not run out
* Avoiding performance bottlenecks

## Failure Handling

* **Detecting :** some types of failures can be detected and some are hard to be certain about.
* **Masking :** some failures that have been detected can be hidden or made less severe;
* **Tolerating :** it is sometimes impractical to try and handle every failure that occurs
* **Recovery :** some failures can recover, for example a rollback mechanism
* **Redundancy :** some failures can be made to tolerate failure using redundant components \(eg multiple services that provide the same service\(failover\)\)

## Concurrency

* Multiple clients can access the same resource at the same time, in some cases for updates.
* One approach to handling concrrency is making access sequential - slows down the system.
* Semaphores supported by the operating system is a well accepted mechanism to handle concurrency.

## Transparency

Hiding certain aspects from the user and application programmer

* Access
* Location
* Concurrency
* Replication
* Failure
* Mobility
* Performance
* Scaling


