
[Resilient distributed datasets: a fault-tolerant abstraction for in-memory cluster computing](https://dl.acm.org/doi/10.5555/2228298.2228301)
[PDF Link](https://www.usenix.org/system/files/conference/nsdi12/nsdi12-final138.pdf)

To address the performance problem in [[MapReduce]] and [[Dryad]] caused by disk operation and the lack of fast data sharing abstraction, an in-memory compute method was proposed named *resilient distributed datasets* (RDDs). 

RDDs ensure the consistency by the read-only attributes, which means a RDD can only be created from data or another RDD. Moreover, RDD also can *lazy compute*, i.e. the content will be computed only when they will be used (until `.count()`, `collect()`, etc. were called), which enable pipeline transformations. All of those features <>

The previous framework transfer data or logs in clusters to ensure that fault tolerance. However, due to the limited of bandwidth and the cost of storage, all the methods are not efficient enough to make high-speed computing possible. Spark prefers to use log to recover the current dataset instead of transfer the whole dataset every operation, which reduce the volume of data need to transfer significantly. Besides, if some RDDs are lost or damaged, computing nodes are also able to reproduce RDDs they should process on.



To make use of RDDs, Spark was implemented and deployed in many areas. After deploying Spark at Google, some strange errors occur frequently. After the investigation, they found those errors are related to cheap memories which do not have erasure coding(?). However, the performance of the cluster is not decrease significantly. The reason is <>. This issue indicates that the <>

Compare with the previous framework, the biggest advantage is the speed. Spark is faster than Hadoop an order of magnitude. Another advantage that cannot be ignored is the latency. Though, Spark cannot process data in near real-time like stream processing, e.g. Apache Storm, but at that time, Spark undoubtedly is an innovation. We also should emphasize that Spark is still widely used nowadays, because Spark provides the interactive data exploration.

Conversely, Spark still has some disadvantages, which might be a trade-off for generalization. Due to the usage of *Scala tuples*, Spark cannot ensure the type safety in compiling. The coarse grained transformations also limit the applications. <>