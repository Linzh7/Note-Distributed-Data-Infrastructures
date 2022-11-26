The engineering side of machine learning used to write custom codes to achieve goal, which leads to a lower code quality and redundant work and some potential vulnerabilities or hazards as results. Therefore, the people working in Google developed a platform which integrates components of machine learning system. However, the questions should be solved is not limited to code quality, the environment difference between training and production also could cause many kinds of failures. Additionally, the commercial products also require lots of features, like stream training and automated pipeline construction. Another important factor is the volume of models. Nowadays, the convolutional neural networks are tended to be too big to training on single computer. The good news is that the management of distributed computing is solved at TensorFlow [1]. What TFX should implement is only the distributed storage system and coordinate all components.

TFX uses TensorFlow as their framework and inherited the flexibility of TensorFlow, which means users can switch different model without reworking the whole project. As we mentioned above, stream training enables model not only fit on the exist dataset, but also could fit the new data. As a commercial product, TFX also provides uniform interface and error handling, resource management procedures. To my surprised, TFX also offers the model validation to ensure the model is fine-tuned and well-trained. 

Comparing with [[ADLS]], which published at the same year, we can easily find that TFX considers more aspects than [[ADLS]], a paper we think more focus on the business value. For example, TFX even considers what if the model is over-fitting and how can we prevent a 'bad' model from deploying to production. On the other hand, there are also some similarity between them. Both of them provide interfaces for users in order to make the whole system transparent and focus on their tasks. Moreover, transfer learning is the inspiration for the concept of warm-starting, [[Giraph++]] is also inspired by vertex-centered model. Both of the pairs are the optimization and development of the prototype. 

Moreover, TFX benefits from the static graph feature of TensorFlow [1], the training and inferring speed is quicker than PyTorch.





In the summary, focus on the main motivations and system design aspects of TFX.


1. [TensorFlow: A System for Large-Scale Machine Learning](https://www.usenix.org/conference/osdi16/technical-sessions/presentation/abadi)