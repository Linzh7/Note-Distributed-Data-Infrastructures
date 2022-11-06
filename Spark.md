
[Resilient distributed datasets: a fault-tolerant abstraction for in-memory cluster computing](https://dl.acm.org/doi/10.5555/2228298.2228301)

To address the performance problem in [[MapReduce]] and [[Dryad]] caused by disk operation and the lack of fast data sharing abstraction, an in-memory compute method was proposed named *resilient distributed datasets* (RDDs). 

The previous framework transfer data or logs in clusters to ensure that fault tolerance. However, due to the limited of bandwidth and the cost of storage, all the methods are not efficient enough to make high-speed computing possible. Spark prefers to use log to recover the current dataset instead of transfer the whole dataset every operation, which reduce the volume of data need to transfer significantly. Besides, if some RDDs are lost or damaged, computing nodes are also able to reproduce RDDs they should process on.


However, after deploying Spark at Google, some strange errors occur frequently. After the investigation, they found those errors are related to cheap memories which do not have erasure coding(?). This issue indicates us that the 

Compare with the previous framework, the biggest advantage is the speed. Spark is faster than Hadoop 1 order of magnitude


We show that Spark is up to 20× faster than Hadoop for iterative applications, speeds up a real-world data analytics report by 40×, and can be used interactively to scan a 1 TB dataset with 5–7s latency.