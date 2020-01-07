# generative-uap

For Fall 2019, I took the Big Data Analytics course at Columbia University (EECS E6893). My project focused on trying to find a generative algorithm for creating universal adversarial perturbations (Inspired by the original UAP paper: [Universal Adversarial Perturbations](https://arxiv.org/abs/1610.08401))

Current algorithms for generating universal adversarial perturbations (UAPs) have dependencies on a training set and/or a model and can take a very long time to generate. The goal of this project was to create a generative uap algorithm that is completely independent of both data (a training set) and models.

The algorithm is based analysis of UAPs generated from [source code from the athors of the UAP paper](https://github.com/LTS4/universal) and two observations:
1) Deep neural networks are able to acheive very complex and organic functions by composing very simple functions (e.g. ReLU)
2) Convolution is a central concept for image classification models

The algorithm is very simple: we iteratively apply a random convolution to a random (padded) seed UAP and saturate the output. 

Below is a GIF that shows the evolution of the UAP over convolution iterations

![UAP Sample #1 GIF](https://github.com/ArmstrongPhysics/generative-uap/blob/master/224x224-samples/rand_conv_224x224_iter45_id00814799.gif)

Below are 224 x 224 sample UAPs generated with the algorithm

![Sample 1](https://github.com/ArmstrongPhysics/generative-uap/blob/master/224x224-samples/rand_conv_224x224_iter45_id00814799.png)

![Sample 2](https://github.com/ArmstrongPhysics/generative-uap/blob/master/224x224-samples/rand_conv_224x224_iter45_id01039413.png)

![Sample 3](https://github.com/ArmstrongPhysics/generative-uap/blob/master/224x224-samples/rand_conv_224x224_iter45_id03036958.png)

![Sample 4](https://github.com/ArmstrongPhysics/generative-uap/blob/master/224x224-samples/rand_conv_224x224_iter45_id08386328.png)

![Sample 5](https://github.com/ArmstrongPhysics/generative-uap/blob/master/224x224-samples/rand_conv_224x224_iter45_id08791660.png)
