# AlexNet-CIFAR10-Tensorflow

This repository contains a Tensorflow implementation of AlexNet, optimized and adapted for the CIFAR-10 dataset ($32 \times 32$ image resolution). 

## The Evolution of AlexNet
AlexNet, introduced by Alex Krizhevsky, Ilya Sutskever, and Geoffrey Hinton, is arguably one of the most influential architectures in the history of deep learning. Winning the 2012 ImageNet Large Scale Visual Recognition Challenge (ILSVRC) by a significant margin, it single-handedly proved that deep convolutional neural networks (CNNs) could be highly effective for complex image classification tasks. 

A key innovation in the original AlexNet was the introduction of the **Dropout layer**. By randomly setting a fraction of input units to zero during training, dropout effectively prevents complex co-adaptations on training data. This drastically reduces overfitting and allows the network to generalize much better to unseen data. This technique was revolutionary at the time and has since become a staple in modern neural network design.

## Modern Enhancements and Optimizations
While the original AlexNet was groundbreaking, modern deep learning practices provide tools to enhance it further. In this project, the classic architecture has been improved to achieve faster convergence and better overall performance on the CIFAR-10 dataset:

- **Batch Normalization**: Introduced to stabilize and accelerate the training process. By normalizing the inputs to each layer, it reduces internal covariate shift, allowing for higher learning rates and significantly faster model convergence.
- **ReLU Activation**: Utilizes Rectified Linear Units (ReLU) throughout the network to combat the vanishing gradient problem and drastically speed up training times compared to traditional activation functions like Tanh or Sigmoid.
- **CIFAR-10 Adaptation**: The network's layer hyperparameters (strides, kernel sizes, and pooling dimensions) have been carefully adjusted to accurately process the smaller $32 \times 32$ spatial resolution of the CIFAR-10 dataset, compared to the original ImageNet inputs.

## Getting Started

### Prerequisites
Ensure you have Python installed along with the required data science and machine learning libraries.

```bash
pip install tensorflow jupyter numpy pandas matplotlib
```

### Running the Project
1. Clone the repository:
```bash
git clone https://github.com/amyas-lab/AlexNet-CIFAR10-Tensorflow.git
cd AlexNet-CIFAR10-Tensorflow
```
2. Open the main notebook:
```bash
jupyter notebook 240166_assignment1_notebook.ipynb
```
3. Run the cells sequentially to initialize, train, and evaluate the enhanced AlexNet model.
