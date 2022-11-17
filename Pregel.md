[Pregel: a system for large-scale graph processing](https://dl.acm.org/citation.cfm?id=1807184)

Graph plays an important role in science experiments, engineering computing and business analysis. For example, the Facebook social network is a graph. Nowadays, the amount of edges and vertices are growth in order of magnitude, which make the graph too big to be analyzed on a single computer. Moreover, large graph also is not easy to process, because it is hard to implement graph algorthms on distributed systems with fault tolerance. 



To address this problem, different organizations have different solutions, Google developed Pregel, and the success of Pregen led to Hadoop's Giraph.

main motivations


system design


put it into context with the rest of the systems we have seen in the course and discuss the respective pros and cons of them.


MapReduce could be used to solve graph problems, but those algorithms are not optimized for graph, which means the performance is not good as our expection. 

, like [[GraphFrames]] on Spark and [[Giraph]] on Hadoop