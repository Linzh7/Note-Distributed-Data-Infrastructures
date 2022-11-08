Hadoop is a distributed framework developed by Apache. There are a number of components are programmed for Hadoop and the core of any system is the storage, the Hadoop Distributed File System (HDFS). 

HDFS and other distributed file system use same strategies to organize storage space. They mark the manager computers as *NameNode* and storage computers as *DataNode*. All transmisions among computers are TCP, which could reduce the transmission error rate.

The biggest difference between HDFS and other systems is that HDFS copies the same data to several DataNodes instead of protect data with RAID. That is a tread-off between data availability and available storage space. This strategy enables user access data from the closest DataNode without other transmisstion, which means it saves lots of bandwidth, the 


NameNodes store the metadata, while DataNodes store the data. 