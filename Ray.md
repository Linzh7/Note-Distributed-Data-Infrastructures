[Ray: A Distributed Framework for Emerging AI Applications](https://www.usenix.org/system/files/osdi18-moritz.pdf)

Nowadays, more and more tasks required an intelligent system which could react to the dynamic environments, reinforcement learning (RL) system. However, due to the features of RL and the 
varies in outcomes with different data, the framework must allow fine-grained calculations, and support heterogeneity in time and resource utilization. Additionally, in order to manage millions of diverse jobs per second with millisecond latencies, dynamic computation is another important 
feature for the framework. Moreover, the solutions developed in recent years are either missing some features or are one-off systems that need to be developed separately for each application. In order to address this problem, the authors proposed an all-in-one system which could handles a wide range of data and the tasks in one system. 

Like the previous systems, Ray also provide a unified interface for the tasks. To solve the biggest challenge, dealing to dynamic workload and stateful computations, Ray proposed interface which can handle task-parallel and actor-based assignments. Another important change is Ray splits the task scheduler and metadata store which contains lineage information and objects in order to provide an instant processing system with lineage-based fault tolerance. Moreover, those systems which only stacking components together cannot address the latency issue. As a result, Ray integrates many existing simulators and deep learning frameworks while guaranteeing very low latency.

If we compare the exist framework with Ray, we can find that the feature of those frameworks cannot satisfy the requirements of RL. [[MapReduce]], [[Spark]] and [[Dryad]] only support coarse-grained operation, while RL need fine-grained data to simulate different environment. TensorFlow and its platform, [[TensorFlow Extended]] does support distributed systems, however, it does not support simulation and serving, which play important roles in RL system.





In addition to purely summarizing the article, put it into context with the rest of the systems we have seen in the course and discuss the respective pros and cons of them.