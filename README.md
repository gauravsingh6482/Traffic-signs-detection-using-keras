# Traffic-signs-detection-using-keras
Traffic signs detection using keras

Traffic Signs Classification with a Convolutional Neural Network
Dataset used: German Traffic Sign Dataset. This dataset has more than 50,000 images of 43 classes.

The dataset used for this project is German Traffic Signs. There are 43 unique traffic signs in the dataset and a quick look at the histogram of the number of samples for each traffic sign shows that they are unevenly distributed. Each image in the dataset is 32 pixels x 32 pixels x 3 Channels (one each for RGB).

Dataset Summary

![traffic sign](https://user-images.githubusercontent.com/68801296/89261509-cf7a2000-d64b-11ea-8857-ad86241a572d.png)


![signs](https://user-images.githubusercontent.com/68801296/89261689-1c5df680-d64c-11ea-81a2-eff7bc779ab5.png)

![Train](https://user-images.githubusercontent.com/68801296/89262067-bd4cb180-d64c-11ea-8d45-782ae8dc74dc.png)

![Valid](https://user-images.githubusercontent.com/68801296/89262086-c5a4ec80-d64c-11ea-8b41-aa141a573cce.png)

![Test](https://user-images.githubusercontent.com/68801296/89262105-cccbfa80-d64c-11ea-8663-3943aa0ba30b.png)

![TrainHist](https://user-images.githubusercontent.com/68801296/89262271-00a72000-d64d-11ea-8ae3-c48871012079.png)


![ValidHist](https://user-images.githubusercontent.com/68801296/89262322-11f02c80-d64d-11ea-95eb-3d478e129cee.png)


![TestHist](https://user-images.githubusercontent.com/68801296/89262341-16b4e080-d64d-11ea-8ec6-7cd8da1fb278.png)

Model Architecture

1. LeNet-5
LeNet-5 is a convolutional network designed for handwritten and machine-printed character recognition. It was introduced by the famous Yann LeCun in his paper Gradient-Based Learning Applied to Document Recognition in 1998. Although this ConvNet is intended to classify hand-written digits, we're confident it have a very high accuracy when dealing with traffic signs, given that both hand-written digits and traffic signs are given to the computer in the form of pixel images.

LeNet-5 architecture:

![LeNet Model (Source Yann LeCun)](https://user-images.githubusercontent.com/68801296/89262516-554a9b00-d64d-11ea-8c2c-0b293d7c10ac.png)

This ConvNet follows these steps:

Input => Convolution => ReLU => Pooling => Convolution => ReLU => Pooling => FullyConnected => ReLU => FullyConnected

Layer 1 (Convolutional): The output shape should be 28x28x6.

Activation. Your choice of activation function.

Pooling. The output shape should be 14x14x6.

Layer 2 (Convolutional): The output shape should be 10x10x16.

Activation. Your choice of activation function.

Pooling. The output shape should be 5x5x16.

Flattening: Flatten the output shape of the final pooling layer such that it's 1D instead of 3D.

Layer 3 (Fully Connected): This should have 120 outputs.

Activation. Your choice of activation function.

Layer 4 (Fully Connected): This should have 84 outputs.

Activation. Your choice of activation function.

Layer 5 (Fully Connected): This should have 10 outputs.

2. VGGNet
VGGNet was first introduced in 2014 by K. Simonyan and A. Zisserman from the University of Oxford in a paper called Very Deep Convolutional Networks for Large-Scale Image Recognition. They were investigating the convolutional network depth on its accuracy in the large-scale image recognition setting. Their main contribution is a thorough evaluation of networks of increasing depth using an architecture with very small (3x3) convolution filters, which shows that a significant improvement on the prior-art configurations can be achieved by pushing the depth to 16-19 weight layers.

VGGNet architecture:

![VGGNet](https://user-images.githubusercontent.com/68801296/89262689-92af2880-d64d-11ea-9054-bee2b4323037.png)

The original VGGNet architecture has 16-19 layers, but I've excluded some of them and implemented a modified version of only 12 layers to save computational resources.

This ConvNet follows these steps:

Input => Convolution => ReLU => Convolution => ReLU => Pooling => Convolution => ReLU => Convolution => ReLU => Pooling => Convolution => ReLU => Convolution => ReLU => Pooling => FullyConnected => ReLU => FullyConnected => ReLU => FullyConnected

Layer 1 (Convolutional): The output shape should be 32x32x32.

Activation. Your choice of activation function.

Layer 2 (Convolutional): The output shape should be 32x32x32.

Activation. Your choice of activation function.

Layer 3 (Pooling) The output shape should be 16x16x32.

Layer 4 (Convolutional): The output shape should be 16x16x64.

Activation. Your choice of activation function.

Layer 5 (Convolutional): The output shape should be 16x16x64.

Activation. Your choice of activation function.

Layer 6 (Pooling) The output shape should be 8x8x64.

Layer 7 (Convolutional): The output shape should be 8x8x128.

Activation. Your choice of activation function.

Layer 8 (Convolutional): The output shape should be 8x8x128.

Activation. Your choice of activation function.

Layer 9 (Pooling) The output shape should be 4x4x128.

Flattening: Flatten the output shape of the final pooling layer such that it's 1D instead of 3D.

Layer 10 (Fully Connected): This should have 128 outputs.

Activation. Your choice of activation function.

Layer 11 (Fully Connected): This should have 128 outputs.

Activation. Your choice of activation function.

Layer 12 (Fully Connected): This should have 43 outputs.

IN this project we are use keras (DEEP LEARNING) library.

![download](https://user-images.githubusercontent.com/68801296/89263006-24b73100-d64e-11ea-87cb-e07c1e62f155.png)


DescriptionKeras is an open-source neural-network library written in Python. It is capable of running on top of TensorFlow, Microsoft Cognitive Toolkit, R, Theano, or PlaidML. Designed to enable fast experimentation with deep neural networks, it focuses on being user-friendly, modular, and extensible.



