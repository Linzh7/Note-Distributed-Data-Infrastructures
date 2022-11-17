[Pregel: a system for large-scale graph processing](https://dl.acm.org/citation.cfm?id=1807184)

Graph plays an important role in science experiments, engineering computing and business analysis. For example, the Facebook social network is a graph. Nowadays, the amount of edges and vertices are growth in order of magnitude, which make the graph too big to be analyzed on a single computer. Moreover, large graph also is not easy to process, because it is hard to implement graph algorthms on distributed systems with fault tolerance. To address this problem, different organizations have different solutions, Google developed Pregel, and the success of Pregen led to Hadoop's Giraph.

To deploy graph computing on distributed system, the first problem should be solved is to propose a method could compuing as a chain instead of a network. This concept also appeared in MapReduce, named narrow dependency. In this case, Pregel use time series to record information, named *supersteps*. In each superstep, vertexes run a user defined function whose parameters are messages sent from other vertexes at the last superstep and send messages to other vertexes. This is an intuitive solution, which is similar with MapReduce. Both of them are focus on the local tasks and ensure this distributed system is efficient. 

To reduce the processing time, the function in each superstep could be parallel

If we put Pregel in the context of previews systems, we can find lots of differences, but also lots of similarities. MapReduce could be used to solve graph problems, but those algorithms are not optimized for graph, which means the performance is not good as our exception. 

, like [[GraphFrames]] on Spark and [[Giraph]] on Hadoop