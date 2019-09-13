# AWS-Certified-Machine-Learning-Study-Notes
AWS Certified Machine Learning – Study Notes

# Learning Path
1. [Linux Academy](https://linuxacademy.com/cp/modules/view/id/340)

# 1. [Machine learning concepts](1-concepts.md)

# 2. [Data](2-data.md)

# 3. [Machine learning models](3-machine-learning-models.md) 

# 4. [Deep Learning](4-deep-learning.md)
# 4. Deep Learning
## Neural Networks
Activation functions:
* **Sigmoid**: Squish number between 0 and 1
* **Tanh**: Squish numbers between -1 and 1
* **ReLU**: Numbers below 0 = 0, all others the same

**Weights**: Weights of the connections between neurons

**Bias**: Added to the sum of inputs to a neuron, to prevent neuron from being deactivated

**Forward propogation**: Go through the network, calculate all weights and biases and to the output layer

**Backwards propogation**: Recalculate weights and biases by analysing loss function using gradient decent 

## Convolutional neural network (CNN)
Classification, mainly image classification

**Filters**: To be learned when building our CNN. 

**Transfer Learning**: Pre-trained filters for edge detection. Taking filters that have been trained on one dataset and use it to train on another without having to start from scratch

## Recurrent Neural Networks (RNN)
Classification, mainly for sequences such as stocks, time-series and text.