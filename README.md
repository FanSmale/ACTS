# ACTS

This is the official implementation for the ACTS algorithm. 

## Model Structure

1. Overall framework

![alt text](https://github.com/FanSmale/ACTS/blob/main/framework.png)

DeepAL framework for hierarchical image classification. In this study, we focus on an information measurement called hierarchical dependency representation entropy (HDRE), a sample selection strategy called approximate class-balanced typical sampling (ACTS), and local probability suppression loss (LPSL). $c_i, i=1, \dots, m$ is the finest level of class label. ``Hierarchical Annotation'' means that the class label is annotated by the oracle in a top-down manner from coarse to fine. However, it is inefficient for a human to annotate the class labels from coarse to fine, hence we introduce a yes-or-no query modality.

3. Sampling bias
   
![alt text](https://github.com/FanSmale/ACTS/blob/main/samplingbias.png)

Sampling bias in AL. For this binary classification problem (prediction red circle/green square), if we sample the data based on uncertainty, then instances close to the decision boundary would be selected. However, their distribution may be very different from that of the population, which misguides the deep model to learn the incorrect data representation. This incorrect guidance appears more obvious when only a small number of label data are available. Note that it is impossible to completely eliminate sampling bias in AL because sampling in AL is not an i.i.d. procedure w.r.t. the underlying distribution, unless simple random sampling is used. Additionally, improving model performance is the ultimate goal of AL rather than eliminating sampling bias.

5. Adaptability of different feature layers in the CNN.
![alt text](https://github.com/FanSmale/ACTS/blob/main/adaptability.png)

The shallow feature layer always reveals texture or shape information, whereas the deep feature layer generally represents semantic information.

## Code Structure:
1. Four folders `CIFAR10, CIFAR100,FashionMNIST,KFPI` are the code for running on different benchmarks.
2. `resnet.py` is the popular resnet structure.
3. `acts.py` is the core sample selection approach, which will be uploaded soon, or contact us for acquiring ``minfan@swpu.edu.cn;yanxuewu2023@163.com''
