[Link](https://www.usenix.org/conference/osdi-04/mapreduce-simplified-data-processing-large-clusters)

In recent years, the volume of data increased rapidly. One of the results was the process of data became difficult. Specifically, we need computers to work as a cluster to deal with the data in order to complete tasks in time. The reason why this technique is appeared in Google is that only those companies need to finish tasks in a short time, in other words, they are sensitive with delay. As a result, to solve this problem, Google proposed a method named MapReduce, which enables to divide a huge task into many subtasks, in order to distribute those subtasks to work nodes. Those functions are easy to understand and implement, which means this framework reduce the threshold for big data processing. Addtionally, It is worth to mention that a high edge server is rare and expensive, whereas the common servers only have limited computing power to handle simple tasks. 

As the name shows, MapReduce can be divided into two parts, the Map function and the Reduce function. The key link between these two parts are key-value pairs. Map function processes on the splitted data into key-value pairs, and Reduce function aggregate the pairs by key



After the paper is published, lots of organizations involved into in this field. Due to the Hadoop, Apache became famous in this area.