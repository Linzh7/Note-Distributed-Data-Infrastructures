
From the perspective of practicality, a system cannot achieve all the three parts: correctness, latency and cost, namely, each project must have a trade-off between them. Therefore, disparate implementers are focused on different area, leading to different systems. Those systems, however, make problems more tricky by trying to give a specific solution. As authors mentioned, we should change our process approach for those problems, that is, give principled abstractions to allow users to make tradeoffs on correctness, latency and cost. For a system like this, the biggest difference is that previous systems focus on the bounded data itself, which conflict with the enormous and disordered data nowadays. 

From this point, Dataflow proposed a unified model which provides flexible model by decomposing pipeline, splits the logical and physical implementation, and enables computing based on event-time with the ability to handle processing time. In this context, we can say that Dataflow is a convenient model for creating data processing pipelines.

Windowing can split the unbounded data into finite chunks in order to do some specific operation. Moreover, Dataflow also offers correct and repeatable results by using watermark to establish a model to measure the skew between event time and processing time. Additionally, the system also need supports for the data windows and signals to inform the end of windows. However, due to the instability of data arrival, global metric cannot satisfy the requirements. They proposed triggers as a result, to provides finer control over windows.

There are also some principles the authors mentioned also impacted on the design of Dataflow. 

[[MapReduce]] is a good start of the field of scale computing, and its successors also have their contribution to build the unified platform, Hadoop. However, the shortcomings, like latency, are also still problems discussed a lot. 

Moreover, MapReduce and others also did not propose a pipeline system to simplify the data process procedure.

[[Spark]] Stream and Storm also enable the processing with low latency and good scalability. However, they cannot offer the exactly-once semantics or limited windowing semantics. 