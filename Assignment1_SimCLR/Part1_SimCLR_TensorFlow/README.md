# SimCLR implementation using TensorFlow - 2

SimCLR is a self supervised learning method. 
Self-supervised learning is a learning technique where the training data is automatically labeled by finding and exploiting correlations between different input features

It uses Contrastive learning approaches, where representations are learned by contrasting positive pairs against negative pairs.

***NOTE: All the notebook needs to be run on GPU***

The colab also experiments with wandb:
Weights & Biases is the machine learning platform to build better models faster. W&B uses lightweight, interoperable tools to quickly track experiments, version and iterate on datasets, evaluate model performance, reproduce models, visualize results and spot regressions, and share findings.

## Dataset
Subset of ImageNet: https://github.com/thunderInfy/imagenet-5-categories

## Implementation:

**Model Architecture:**

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment1_SimCLR/Part1_SimCLR_TensorFlow/ScreenShots/Model_Architecture.png" width="400">

**Contrastive Learning process - SimCLR:**

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment1_SimCLR/Part1_SimCLR_TensorFlow/ScreenShots/ContrastiveLearning_1.png" width="400">

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment1_SimCLR/Part1_SimCLR_TensorFlow/ScreenShots/ContrastiveLearning_2.png" width="400">

**Model Evaluation**

Linear model - With resnet_simclr.layers[-2]

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment1_SimCLR/Part1_SimCLR_TensorFlow/ScreenShots/resnet_simclr_layers[-2].png" width="400">

Linear model - With resnet_simclr.layers[-4]

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment1_SimCLR/Part1_SimCLR_TensorFlow/ScreenShots/resnet_simclr_layers[-4].png" width="400">

Linear model - With resnet_simclr.layers[-6]

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment1_SimCLR/Part1_SimCLR_TensorFlow/ScreenShots/resnet_simclr_layers[-6].png" width="400">

With only the base encoder network - without any non-linear projections

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment1_SimCLR/Part1_SimCLR_TensorFlow/ScreenShots/No_nonlinear.png" width="400">

Representations with one hidden layer - ReLu

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment1_SimCLR/Part1_SimCLR_TensorFlow/ScreenShots/one_relu.png" width="400">

Representations with 2 hidden layers - ReLu

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment1_SimCLR/Part1_SimCLR_TensorFlow/ScreenShots/2_relu.png" width="400">

## References:
1. https://github.com/sayakpaul/SimCLR-in-TensorFlow-2
2. https://docs.wandb.ai/
3. https://medium.com/analytics-vidhya/understanding-simclr-a-simple-framework-for-contrastive-learning-of-visual-representations-d544a9003f3c
