---
id: 88XPYXVcgyD0r9T332u0n
title: CAP
desc: ''
updated: 1642294330942
created: 1642294083508
---

# CAP \(or more accurately PACELC\) theorem

CAP Theorem asserts that you can only have two of the three, Consistency, Availability or Partition tolerance. However, Partition tolerance must be in place, we do not have the choice to drop Partition tolerance.

PACELC states that in the absence of partitions, you will still have to choose between latency and consistency.

Probabilistic Bounded Staleness \(PBS\) helps us here, it can emperically give a probability to the staleness of our data!.

But interestingly, we dont always have to choose one of CAP, if you drop support for update operations, it is possible to have all three!!

## Resources

* [http://nathanmarz.com/blog/how-to-beat-the-cap-theorem.html](http://nathanmarz.com/blog/how-to-beat-the-cap-theorem.html)
* [https://codahale.com/you-cant-sacrifice-partition-tolerance/](https://codahale.com/you-cant-sacrifice-partition-tolerance/)


