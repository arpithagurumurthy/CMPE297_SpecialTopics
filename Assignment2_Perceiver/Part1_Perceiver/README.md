# **Perceiver model implementation for image classification**

* Dataset: CIFAR-100 dataset - 
  * The CIFAR-10 dataset consists of 60000 32x32 colour images in 10 classes, with 6000 images per class.
  * CIFAR-100 dataset is just like the CIFAR-10, except that it has 100 classes containing 600 images each. 
  * There are 500 training images and 100 testing images per class. The 100 classes in the CIFAR-100 are grouped into 20 superclasses. 
  * Each image comes with a "fine" label (the class to which it belongs) and a "coarse" label (the superclass to which it belongs).
* The Perceiver model leverages an asymmetric attention mechanism to iteratively distill inputs into a tight latent bottleneck, allowing it to scale to handle very large inputs.
* The perception models used in deep learning are designed for individual modalities, often relying on domain-specific assumptions such as the local grid structures exploited by virtually all existing vision models

***Note: tensorflow-addons should be installed***

## Model structure
Perceiver architecture is built from two components:
* a cross-attention module that maps a byte array (e.g. an
pixel array) and a latent array to a latent array, and 
* a Transformer tower that maps a latent array to a latent array

## Model training
The hyperparameter values are -
* patch_size = 2 
* num_patches = (image_size // patch_size) ** 2  
* latent_dim = 256
* projection_dim = 256
* num_heads = 8
* num_transformer_blocks = 4
* num_iterations = 2

Training results:

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment1_SimCLR/Part1_SimCLR_TensorFlow/ScreenShots/resnet_simclr_layers[-2].png" width="400">

* After 35 epochs, the Perceiver model achieves around 50% accuracy on the test data.
* Best accuracy:
  * Test accuracy: 51.62%
  * Test top 5 accuracy: 78.75%


## **References:**
* https://keras.io/examples/vision/perceiver_image_classification/
* https://colab.research.google.com/github/keras-team/keras-io/blob/master/examples/vision/ipynb/perceiver_image_classification.ipynb
* https://arxiv.org/pdf/2103.03206.pdf
* https://www.cs.toronto.edu/~kriz/cifar.html


