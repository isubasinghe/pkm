---
id: KxCogPE8ArRppcjxehXKM
title: Failure Model
desc: ''
updated: 1642295002660
created: 1642294943996
---
# Failure Model
The failures in processes and channels are presented using the following taxonomy:
* Omission failures 
* Arbitrary failures
* Timing failures

## Omissions Failures
Omission failures refers to cases where a process or a communication channel fails to perform what is expected to do.
  * Process omission failures:
    * Normally caused by a process crash
    * Repeated failures during invocation is an indication
    * Timeouts can be used to detect this type of crash 
    * A crash is referred to as __fail-stop__ if other processes can detect certainly that the process crashed. 

### Communication omission failure could be to: 
  * Send omission failure: A message not being transported from sending process to its outgoing buffer. 
  * Recieve omission failure: A message not being transported from the receiving process's incoming message buffer and the receiving process. 
  * Channel omission failures: A message not being transported from **p**'s outgoing message buffer to **q**'s incoming message buffer.

## Arbitrary Failures (Byzantine failure)
Refers to any type of failure that can occur in a system. Could be due to: 
  * Intended steps omitted in processing
  * Message contents corrupted 
  * Non-existent messages delivered 
  * Real messages delivered more than once

## Omission and arbitrary failures
| Class of failure |      Affects       |                                                Description                                                |
| :--------------: | :----------------: | :-------------------------------------------------------------------------------------------------------: |
|    Fail-stop     |      Process       |                  Process halts and remains halted. Other processes may detect this state                  |
|      Crash       |      Process       |                  Process halts and remains so. Other processes may not detect this state                  |
|     Omission     |      Channel       | A message inserted in an outgoing message buffer never arrives at the other end's incoming message buffer |
|  Send-omission   |      Process       |                      Process attempts send but message not placed in outgoing buffer                      |
| Receive-omission |      Process       |                    Message received in incoming buffer but process does not receive it                    |
|    Arbitrary     | Process or channel |                                                                                                           |


## Timing Failures

Occurs when time limits set on process execution time, message delivery time
and clock rate drift. They are particularly relevant to synchronous systems and less relevant to asynchronous systems since the latter usually places no or less strict bounds on timing. 

| Class of failure | Affects |                                 Description                                  |
| :--------------: | :-----: | :--------------------------------------------------------------------------: |
|      Clock       | Process | Process's local clock exceeds the bounds on its rate of drift from real time |
|   Performance    | Process |         Process exceeds the bounds on the interval between two steps         |
|   Performance    | Channel |         A message's transmission takes longer than the stated bound          |

