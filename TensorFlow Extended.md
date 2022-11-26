The engineering side of machine learning used to write custom codes to achieve goal, which leads to a lower code quality and redundant work and some potential vulnerabilities or hazards as results. Therefore, the people working in Google developed a platform which integrates components of machine learning system. However, the questions should be solved is not limited to code quality, the environment difference between training and production also could cause many kinds of failures. Additionally, the commercial products also require lots of features, like stream training and automated pipeline construction. Another important factor is the volume of models. Nowadays, the convolutional neural networks are tended to be too big to training on single computer. The good news is that the management of distributed computing is solved at TensorFlow [1]. What TFX should implement is only the distributed storage system and coordinate all components.

TFX uses TensorFlow as their framework and inherited the flexibility of TensorFlow, which means users can switch different model without reworking the whole project. As we mentioned above, stream training enables model not only fit on the exist dataset, but also could fit the new data. As a commercial product, TFX also provides uniform interface and error handling, resource management procedures. To my surprised, TFX also offers the model validation to ensure the model is fine-tuned and well trained.



Moreover, TFX benefits from the static graph feature of TensorFlow [1], the training and inferring speed is more quicker than PyTorch.





In the summary, focus on the main motivations and system design aspects of TFX.

In addition to purely summarizing the article, put it into context with the rest of the systems we have seen in the course and discuss the respective pros and cons of them.



1. [TensorFlow: A System for Large-Scale Machine Learning](https://www.usenix.org/conference/osdi16/technical-sessions/presentation/abadi)