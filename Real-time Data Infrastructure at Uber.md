[Real-time Data Infrastructure at Uber](https://dl.acm.org/doi/10.1145/3448016.3457552)

Uber is a company provides vary fields services, and some of the services need to make decision in seconds. Moreover, Uber also wants to explore stream data to difference roles with a huge volume of data. Therefore, Uber refined Apache ecosystem to satisfy their requirements.

The structure of data processing system in Uber is a modified version of Apache. This is a hierarchical system, which could be broadly divided into three layers: storage, streaming and computation, analyzation. 

There are two data types should be stored in this system, living streaming data and archival data from the whole system. The latter use [[HDFS]] to guarantee the fault-tolerance, meanwhile, the former use Kafka to provide streaming storage. Because data in PB magnitude uploaded to Uber every day, the processing system must support large scale. Therefore, Uber proposed cluster federation and dead letter queue.(addmore? like features of kafka)

The scale and workloads impact not only on storage, but also on steaming and computation. Flink is a high-performance engine in industry, which has good back pressure handling ability comparing with Strom and less memory comsuming than [[Spark]]. Though Flink is a great choice, there are still some shortcomings need to overcome. Therefore, Uber improved its basic query function.

For a company, analyzation is important. Therefore, Uber uses Apache Pinot, an online analytical processing system, for high-level query and analyze with low latency and TB-scale data support.  Uber also modifies Pinot a lot to meet the demand, specifically, fine-grained semantics and full SQL support. Moreover, Presto is also involved in this part to provide flexiable and extensible in-memory query.


