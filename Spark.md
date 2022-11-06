
[Resilient distributed datasets: a fault-tolerant abstraction for in-memory cluster computing](https://dl.acm.org/doi/10.5555/2228298.2228301)

To address the performance problem in [[MapReduce]] caused by disk operation, an in-memory was proposed by f

Besides, Spark prefer to use a limited shared memory instead of updating the mutual exclusion everytime.


However, after deploying Spark at Google, some strange errors occur frequently. After the investigation, they found those errors are related to cheap memories which do not have erasure coding. This issue indicates us that the 