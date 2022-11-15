[Azure Data Lake Store: A Hyperscale Distributed File Service for Big Data Analytics](https://dl.acm.org/doi/10.1145/3035918.3056100)

Due to the development of IoT, people are eager to explore hundreds petabytes data in an interactive way with a low price. To achieve this goal, Microsoft has to develop a system that is both efficient and reliable, the ADLS.

## put it into context with the rest of the systems we have seen

The previous data process systems have some disadvantages and thus can not provide an efficient analyze system. Spark only offers coarse-grained data, which means nodes will spend some time to searching the data we need. Another example is that MapReduce uses disks to storage data, and it also takes time to read the data from the disk to computing. Also, as we mentioned above, we also should control the permission to data, because ADLS is an open business services.

## system design

The key concept of ADLS is tiered storage, includes local tiers and remote tiers. Local tiers could provide a quick access, while remote tiers support different storage systems, and provides abstracts for futher use.



Because of the motivations, a data block in ADLS is only 4 megabytes. As we know, handling multiple partitions of files is a challenge. To achieve the consistency, ADLS proposed states named *sealed* and *unsealed*. If one partition can connect to the next partition, it will be labeled as *sealed*. For the last partition, if the whole file will not be changed anymore, then the last partition will be marked as *sealed*. Moreover, UIDs are used to mark any partition, and ADLS maintains the list of UIDs to track any file. 




Because ADLS is a PaaS, the access permission to data is another important thing. 




## discuss the respective pros and cons of them
