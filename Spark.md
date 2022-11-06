
[Resilient distributed datasets: a fault-tolerant abstraction for in-memory cluster computing](https://dl.acm.org/doi/10.5555/2228298.2228301)

To address the performance problem in [[MapReduce]] and [[Dryad]] caused by disk operation and the lack of fast data sharing abstraction, an in-memory compute method was proposed named *resilient distributed datasets*. 

The previous framework transfer data or logs in clusters to ensure that fault tolerance. However, due to the limited of bandwidth and the cost of storage, all the methods are not efficient enough to make high-speed computing possible.

Besides, Spark prefer to use a limited shared memory instead of updating the mutual exclusion everytime(?).


However, after deploying Spark at Google, some strange errors occur frequently. After the investigation, they found those errors are related to cheap memories which do not have erasure coding(?). This issue indicates us that the 