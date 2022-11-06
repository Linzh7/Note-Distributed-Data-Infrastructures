
[Resilient distributed datasets: a fault-tolerant abstraction for in-memory cluster computing](https://dl.acm.org/doi/10.5555/2228298.2228301)

To address the performance problem in [[MapReduce]] and [[Dryad]] caused by disk operation and the lack of fast data sharing abstraction, an in-memory compute method was proposed named *resilient distributed datasets* (RDDs). 

RDD is 

The previous framework transfer data or logs in clusters to ensure that fault tolerance. However, due to the limited of bandwidth and the cost of storage, all the methods are not efficient enough to make high-speed computing possible. Spark prefers to use log to recover the current dataset instead of transfer the whole dataset every operation, which reduce the volume of data need to transfer significantly. Besides, if some RDDs are lost or damaged, computing nodes are also able to reproduce RDDs they should process on.


However, after deploying Spark at Google, some strange errors occur frequently. After the investigation, they found those errors are related to cheap memories which do not have erasure coding(?). This issue indicates us that the 

Compare with the previous framework, the biggest advantage is the speed. Spark is faster than Hadoop an order of magnitude. Another advantage that cannot be ignored is the latency. Though, Spark cannot process data in near real-time like stream processing, e.g. Apache Storm, but at that time, Spark undoubtedly is an innovation. We also should emphasize that Spark is still widely used nowadays, because Spark provides the interactive data exploration.

Conversely, Spark still has some disadvantages, which might be a trade-off for generalization. Due to the usage of *Scala tuples*, Spark cannot ensure the type safety in compiling. 