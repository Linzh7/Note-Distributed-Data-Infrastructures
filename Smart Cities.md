[Building a Big Data Platform for Smart Cities: Experience and Lessons from Santander](https://ieeexplore.ieee.org/abstract/document/7207275/)

As the development of industry, IoT also get involved in our daily lives. However, how to process those data became the new question for analyzer. CiDAP is the platform to address this question. 

The architecture of the smart city system can be divided into two parts: SmartSantander, the smart city testbed, and CiDAP, the live city data and analytics system. The latter one provides the ability of processing data in different time type, such as historical data, neartime data, and real-time. Moreover, This system can also process semi-structured data and unstructured data.

Furthermore, the architecture of CiDAP is also worth to discuss. Generally, CiDAP have a hierarchical structure, specifically, there are three layers in CiDAP. The first layer, data sources layer, is made up by millions of sensors and cameras, moreover, there are IoT-agent which could represent these sensors and response to the higher layer. Then, the second layer is the processing and storage layer, we will explain its details below. The top layer is the application layer, which are deployed applications to build interfaces for public or enable analyzers and scientists to explore the data.

Because the data sources upload semi-structured data and unstructured data, the processing layer must be able to handle both of them. 

The semi-structured, JSON data, is stored as JSON file in NoSQL database, CouchDB. The reason why they use CouchDB as their storage system is that CouchDB is able to work more closely with other components. For instance, CouchDB can generate and update map-reduce based view, provides API to enable other components to read and write data directly. 

The processing of data, however, can be categorized as internal and external. The internal process happens in CouchDB, which can reduce the overhead of transmisstion. However, if the computing task is more complex




Also, write about the various components, how they are integrated and contrast the lessons learned to what we have seen in the course.