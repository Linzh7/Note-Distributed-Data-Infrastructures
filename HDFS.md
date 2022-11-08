Hadoop is a distributed framework developed by Apache. There are a number of components are programmed for Hadoop and the core of any system is the storage, the Hadoop Distributed File System (HDFS). 

HDFS and other distributed file system use same strategies to organize storage space. They mark the manager computers as *NameNode* and storage computers as *DataNode*. All transmisions among computers are TCP, which could reduce the transmission error rate. The metadata stored at NameNode are the records of permission, date, namespace, etc., which are maintained at memory to increase the access speed. Also, these metadata have backups and logs to improve fault-tolerance. Additionally, NameNodes could also play another role in HDFS, *CheckpointNode* or *BackupNode*. CheckpointNode usually downloads the recent checkpoint and logs, then combines them to get a new checkpoint and return it to NameNode. BackupNode is more like a shadow of NameNode, it will not only creates checkpoint also maintains a real-time image of NameNode. Both are designed to improve the fault tolerance of NameNode.

The biggest difference between HDFS and other systems is that HDFS copies the same data to several DataNodes instead of protect data with RAID. That is a tread-off between data availability and available storage space. This strategy enables user access data from the closest DataNode without other transmisstion, which means it saves lots of bandwidth, the most important resources in the data warehouse. HDFS stores data in three different DataNodes by default. It is also worth to mention that the choice of three DataNodes. The first DataNodes and the second DataNodes is located at the same rack, while the third DataNodes should be located at a different rack. This strategy named *rack awareness policies* and it is aimed to improve the write performance and save bandwidth while not harm to fault-tolerance. Specifically, if one rack faces power problem, there still other copy(s) are available. The two copies on the same rack could reduce the traffic between racks, instead, they use ToR switch to copy data. Moreover, these policies also allow the NameNode distribute tasks to the cloest DataNode, which reduce the latency of compuing. There is a report that claim that most operation will have a good performance when the free disk space is greater than 40%. Therefore, HDFS also keep the load balance among DataNodes by a tool named balancer.

![[Pasted image 20221108175156.png]]

Another important policie is the communication between NameNodes and DataNodes. Beside the regular storage report from DataNodes, they also use heartbeats to make sure that DataNodes are still accessible. Moreover, NameNodes will not communicate to DataNodes dirctly, instead, NameNodes send information by replying heartbeats.

From the Brewer’s CAP theorem, the I/O operation is usually the trickiest part in distributed systems, as those systems should always keep partition tolerance. The result of the tread-off is that HDFS gives up a certain level of availability, because the authors acknowledge that we cannot certain the time to process an operation. Conversely, we can see that did well in consistency and partition tolerance by lease and verifying data with namenode.







