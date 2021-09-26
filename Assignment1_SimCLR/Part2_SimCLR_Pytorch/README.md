# SimCLR implementation using Pytorch

SimCLR or Simple Framework for Contrastive Learning of Visual Representations is a State-of-the-art Self-supervised Representation Learning Framework.
SimCLR is a self supervised learning method. Self-supervised learning is a learning technique where the training data is automatically labeled by finding and exploiting correlations between different input features

It uses Contrastive learning approaches, where representations are learned by contrasting positive pairs against negative pairs.

*Colab Pro was used to execute the implementation*

# Main article used as Reference:
https://medium.com/the-owl/simclr-in-pytorch-5f290cb11dd7

# Dataset:
CIFAR10 dataset
*Note: Authors of the original simclr paper used this dataset too*

**Feature results after using TSNE**

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment1_SimCLR/Part2_SimCLR_Pytorch/ScreenShots/TSNE_BaseEncoder.png" width="400">

*TSNE-fied features from the output of the base encoder after 100 epochs of training*

**Loss curve for the same:**

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment1_SimCLR/Part2_SimCLR_Pytorch/ScreenShots/Loss_curve.png" width="400">

**Training Results**

```Training and validation Accuracy```

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment1_SimCLR/Part2_SimCLR_Pytorch/ScreenShots/Training_accuracy.png" width="400">

```Training and validation Loss```

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment1_SimCLR/Part2_SimCLR_Pytorch/ScreenShots/Training_Loss.png" width="400">


