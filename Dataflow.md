
From the perspective of practicality, a system cannot achieve all the three parts: correctness, latency and cost, namely, each project must have a trade-off between them. Therefore, disparate implementers are focused on different area, leading to different systems. Those systems, however, make problems more tricky by trying to give a specific solution. As authors mentioned, we should change our process approach for those problems, that is, give principled abstractions to allow users to make tradeoffs on correctness, latency and cost. For a system like this, the biggest difference is that previous systems focus on the bounded data itself, which conflict with the enormous and disordered data nowadays.

From this point, Dataflow proposed a unified model which provides flexible model by decomposing pipeline, splits the logical and physical implementation, and enables computing based on event-time with the ability to handle processing time. In this context, we can say that Dataflow is a convenient model for creating data processing pipelines.

Windowing can split the unbounded data into finite chunks in order to do some specific operation. Moreover, Dataflow also are 


  

In addition to purely summarizing the article, put it into context with the rest of the systems we have seen in the course and discuss the respective pros and cons of them.


[[MapReduce]] is a good start of the field of scale computing, and the shortcomings, like latency, are also discussed a lot.

[[Spark]] Stream and Storm also enable the processing with low latency and good scalability. However, they cannot offer the exactly-once semantics or limited windowing semantics. 