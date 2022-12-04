
From the perspective of practicality, a system cannot achieve all the three parts: correctness, latency and cost, namely, each project must have a trade-off between them. Therefore, disparate implementers are focused on different area, leading to different systems. Those systems, however, make problems more tricky by trying to give a specific solution. As authors mentioned, we should change our process approach for those problems, that is, give principled abstractions to allow users to make tradeoffs on correctness, latency and cost. For a system like this, the biggest difference is that they focus on the data itself, which conflict with the enormous and disordered data nowadays.



main motivations and system design aspects of the system presented in the paper.  


Window


  

In addition to purely summarizing the article, put it into context with the rest of the systems we have seen in the course and discuss the respective pros and cons of them.


MapReduce is a good start of the field of scale computing, and the shortcomings, like latency, are also discussed a lot.

Spark Stream and Storm also enable the processing with low latency and good scalability. However, they cannot offer the exactly-once semantics or limited windowing semantics. 