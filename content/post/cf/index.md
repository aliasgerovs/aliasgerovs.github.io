---
title: "Measuring Catastrophic Forgetting in Neural Networks. Proceedings of the AAAI Conference on Artificial Intelligence, 32(1)." 
summary: "A summary of the same paper"
date: 2023-09-13
math: true
featured: false
authors: 
 - admin
tags: 
 - catastrophic forgetting
 - neural networks
 - lifelong learning 
 - deep learning
 - machine learning
 - supervised learning 
 - incremental learning

categories: 
 - Paper Reviews 
---

## Overview
The paper discusses the challenges associated with deep neural network when it comes to **incremental learning** and **catastrophic forgetting**. Catastrophic forgetting is the issue once a neural network is trained for a specific task, it is challenging to adapt it to new tasks without forgetting the knowledge it has gained from previous tasks. Also, it mentions that **various methods and solutions** have been proposed to address this issue, but there is **no comprehensive evaluation** of those methods in the different types of the real-world data. As a proposed solution to show that, paper emphasizes the need for evaluating these mechanisms - regularization, ensembling, rehearsal, dual-memory models, and sparsecoding using new metrics and benchmarks. This is important because the current evaluations are inconsistent and often conducted on **small-scale problems like MNIST**.
Paper says that while we are talking about the high accuracy of DNNs methods today, we still need to accept that catastrophic forgetting issue **has not been still solved**, we can see it from the simple MLP – Multi Layer Perceptron models as there is inability of standard DNN architectures and training algorithms to handle incremental learning without experiencing catastrophic forgetting. There is still need for retraining still, which could be not possible to do that all the time due to being time-consuming and **computationally intensive**, especially when dealing with large datasets. 


## Approach

For conducting the study, paper use MLP incrementally trained for the classification tasks. 

**Dataset organization:** The labeled training dataset, denoted as D, is structured into multiple study sessions or batches, represented as {Bt} for t = 1 to T. Each study session Bt consists of a varying number of labeled training data points, with Nt data points in session t. Each data point is represented as (xj, yj) where xj is the feature vector of dimension d, and yj is a discrete label. 

**Sequential Learning:** The neural network is allowed to learn from these study sessions sequentially, in order they are presented. It means that in time t, neural network can only learn from the training session Bt. Network is also allowed to use auxiliary memory to store information from previous sessions which needs to be reported.

**Non-IID Data**: As some batches could have the data which is not identically and independently distributed across all categories, data is assumed **non-IID here**.

**Evaluation**: The paper says that during the training process, between the training sessions model may undergo testing over the test data since the primary aim here is the assessing of how well the model retains knowledge from previous sessions when learning new ones.

Paper explains how **“Catastrophic Forgetting**” occur with clearly mentioning that **stability-plasticity** dilemma. Network requires plasticity in order to learn new tasks, but at the same time once there are high weight fluctuations, model starts to forget the previously learned data. It explains that while keeping the weights stable could solve the issue, but it prevents model to learn new training data. That is why it is called stability-plasticity dilemma.
Here are **two main approaches** that are mentioned by paper. The first one is keeping the old and new representations separate, which could be done using **distributed models, regularization and ensembling.** The second one is combining new and old data and training on merged data, which is not the desired case when the data size is huge, as explained at the beginning of the review.


## Previous Work
Goodfellow and other have compared the different **activation functions** and **learning algorithms**, even though both are not designed for solving the catastrophic forgetting but it is commonly concluded that learning algorithms have **larger impact** on that which is the focus of the paper. 

Paper also talks about **Evolved Plastic ANN** that has been studied by Soltoggio, Stanley and Risi, where neural networks can establish the plasticity with time but still there was no established benchmarks for the comparison of the performance of that networks over different real-world datasets.

**How to mitigate Catastrophic Forgetting?**

Previously suggested **5 approaches** have been discussed in the paper.
**Regularization**: It describes the idea here is addition of the constraints to the weight updating process. The approach proposed has **fast** and **slow** weights, where the former one has the plasticity where it is affected by the updates considerably, while the latter one has the stability which is hardly affected by the weights updates and as a result it remembers the previous learned data. Here EWC is used for the evaluation of the regularization. 

**Ensemble Methods:** Here the idea is explicitly or implicitly training classification NN models and ensembling them for the prediction. For the explicite ensembling method, **multiple sub-neural** networks are being trained for each new session, however memory usage is increased a lot in that case. There are some approaches for alleviating this issue, **Accuracy Weighted Ensembles**, and **Life-long Machine Learning** which are automatically deciding which subnets should be added to the ensemble. For the implicite ensembling method, **PathNet** is the one of the proposed solutions, which finds the optimal path in the neural network for each learning session and it keeps those paths frozen, and when new sessions learned previous ones are not forgotten. PathNet is used here for the evaluation of the ensemble methods.

**Rehearsal Methods:** Here the described idea is rehearsal methods try to **mix data** from the earlier sessions with the current session data to mitigate the CF. The main border here is the need for the storing of the previous data which is **costly**. There is also pseudorehersal methods which are used to generate patterns that are combined with the current training session. 
Here is also **GeppNet**, which uses self-organizing map SOM as a hidden layer to topologically recognize the data from the input layer and clustering it to **2-D lattice**. Here to evaluate the rehearsal methods GeppNet is being used.

**Dual-Memory Models:** The paper describes of the dual memory models have been adapted from the mammalian brain, which is assumed to store memories in two distinct spheres, hippocampus and pre-frontal cortex. Dual Memory Models uses rehearsal methods but not all rehearsal methods use Dual-Memory models. Paper uses GeppNet and GeppNet + STM (Short Term Memory) for the evaluation of the dual memory models which is used for mitigating the CF issue.

**Sparse-Coding Methods:**
The paper explains **interference** between new and previously learned representations in the neural network as one of the primary reasons for the catastrophic forgetting issue. Sparse-Coding methods can reduce the chance of interference however it could ruin the generalization. It talks about two methods here **CALM** and **ALCOVE**, where former one is searching for the node which has not been dedicated for showing other information or concept while latter one ALCOVE is shallow neural network uses distance-based representation which result in keeping weights unchanged even there is new data learned.

**Evaluation of the Models**
Five models have been evaluated in this paper, namely **EWC, PathNet, GeppNet, GeppNet+STM, and FEL**. The number of parameters to be used across all models, used bas MLP model which performed well for CUB-200 dataset and Audio Set when training in **offline mood**, the process of training a machine learning model on a fixed dataset in advance, without real-time adaptation to new data. To provide fairness in the comparison the number of parameters in the incremental learning has been chosen as much as close to the base MLP setup. 

**Elastic Weight Consolidation:** 

- EWC adds an additional constraint to the loss function, and directly plasticity away from the weights that contribute most to the previous tasks.

**PathNet:**

- Utilizes a genetic algorithm to find an optimal learning path.
- Creates a new output layer for each learning session to retain previous session data.
- Risks losing learning ability if the network's capacity is exceeded, potentially overwriting valuable information.
- Each path in PathNet has its own set of weights, updated independently.
- This independence can lead to inefficient resource allocation, with some paths becoming overly specialized while others remain underutilized.

**GeppNet:**

- A biologically inspired model that addresses forgetting by rehearsing information.
- Utilizes a Self-Organizing Map (SOM) to project input data into a 2D lattice.
- Initially trains on the first session and then learns subsequent sessions incrementally.
- Updates the SOM layer and classification layer when detecting novel data.
- GeppNet+STM variant stores novel data in a short-term memory buffer and replays it during the sleep phase.
- Capable of making real-time predictions by determining memory location in short-term or long-term storage.

**Fixed Expansion Layer (FEL):**

- Uses sparsity within a neural network featuring two hidden layers to prevent catastrophic forgetting.
- The second hidden layer (FEL-layer) has more capacity but utilizes sparse, fixed weights.
- Partially connected to the first hidden layer, with only some FEL layer units contributing to the final output.
- This design preserves knowledge while learning new tasks, preventing catastrophic forgetting.


**Experiments and Results**

**Dataset selection:** As stated before, paper reiterate on the point that today CF mitigating methods have not been properly tested on the real-world datasets. Here the reasons for the choosing CUB-200, AudioSet and MNIST is due to having large number of classes, small number of samples in some classes, and different data modalities namely image and audio.
For the comprehensive evaluation, different benchmarks settled up for the model performance. 
Data Permutation Experiment: Which is permutation of the feature vector across sessions, and then evaluation of the models’ performance how it recalls the previous training’s data.

**Incremental Class Learning:** Model will learn each class in new session after learning the base set.

**Multi-Modal Learning:** Model will learn different datasets, for example data for image classification and then data for audio classification and then evaluation of how model performs.


**Metrics**: Here three different types of metrics suggested by paper. 

- αnew,i - The test accuracy for session i immediately after it is learned.
- αbase,i - Test accuracy on the first session.
- αall, i - Test accuracy on the all sessions.
- αideal,i - Offline MLP accuracy on the base set, which we assume is the ideal performance.

**Results**

**Data Permutation Experiment:**
- PathNet performed best overall in data permutation experiments, except for CUB-200.
- PathNet requires information about the session during testing, potentially giving it an unfair advantage.
- PathNet saturates quickly due to the lack of feature sharing, leaving only the output layer trainable.
- GeppNet variants excelled at incremental class learning.
- EWC was the second-best performer in data permutation experiments, redirecting plasticity instead of freezing weights.
- GeppNet+STM performed well at retaining the base set but struggled with new classes.
- FEL improved significantly but had a 40x memory footprint increase, suggesting it may not be ideal for deployment.

**Multi-Modal Experiment:**
- EWC performed best in multi-modal experiments, possibly because features between modalities were non-redundant.
- PathNet may work better with data having different but not entirely dissimilar representations.

**Memory and Efficiency:**
- PathNet and GeppNet variants have different memory usage and training speed.
- PathNet creates a new output layer for each session, making it slow in some tasks.
- Models that expand as sessions increase or store data from prior sessions may have limited real-world application due to memory constraints.
- Memory footprint should be considered when comparing models for incremental learning.
- Metrics can be adapted to other training paradigms like reinforcement learning or unsupervised learning.

**Optimal Performers:**
- A combination of rehearsal/pseudo-rehearsal and dual-memory systems were optimal for incremental class learning.
- Regularization and ensembling worked best for separating dissimilar sessions in a common DNN framework.

## Conclusion

Catastrophic forgetting is not solved by any single method; combinations of mechanisms are needed.
Future work should involve using larger and more challenging datasets in lifelong learning research.


## References
- [Measuring catastrophic forgetting in neural networks](https://ojs.aaai.org/index.php/AAAI/article/view/11651)