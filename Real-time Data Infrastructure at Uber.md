[Real-time Data Infrastructure at Uber](https://dl.acm.org/doi/10.1145/3448016.3457552)

Uber is a company provides vary fields services, and some of the services need to make decision in seconds. Moreover, Uber also wants to explore stream data to difference roles with a huge volume of data. Therefore, Uber refined Apache ecosystem to satisfy their requirements.

The structure of data processing system in Uber is a modified version of Apache. This is a hierarchical system, which could be broadly divided into three layers: storage, pipelines

we can start with the data pipeline, streaming. Every day, data in PB magnitude upload to Uber, which indicate the processing system must support large scale with numerous faults. Therefore, Uber replaces the default failure handling mechanism with dead letter queue which provides non-blocking retry to improve the traffic 

basic part, storage. To achieve the consistency, 

focus on how the overall system architecture is designed.   



Also, write about the various components, how they are integrated and contrast the lessons learned to what we have seen in the course.