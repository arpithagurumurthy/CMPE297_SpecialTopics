# HW5: Meta learning and multi task learning

* Few-shot learning is the problem of making predictions based on a limited number of samples. 
* The goal is not to let the model recognize the images in the training set and then generalize to the test set. 
* **Instead, the goal in few-shot learning is to learn. “Learn to learn” sounds hard to understand.**
* It means making classification or regression based on a very small number of samples
* We do not train a big model using a big training set. Rather than training the model to recognize specific objects such as tigers and elephants in the training set, we train the model to know the similarity and differences between objects.
* **Few-shot learning is a kind of meta-learning**
* Multi-task learning (MTL) is a subfield of machine learning in which multiple learning tasks are solved at the same time, while exploiting commonalities and differences across tasks

## CMPE297_HW5_MAML.ipynb

* **Dataset:** Implements the reptile MAML algorithm for meta learning on the Omniglot dataset. 
* This is a dataset of 1,623 characters taken from 50 different alphabets, with 20 examples for each character.
* The Reptile algorithm was developed by OpenAI to perform model agnostic meta-learning. 
* Specifically, this algorithm was designed to quickly learn to perform new tasks with minimal training (few-shot learning). 
* The algorithm works by performing Stochastic Gradient Descent using the difference between weights trained on a mini-batch of never before seen data and the model weights prior to training over a fixed number of meta-iterations.

The below screenshot represents the model architecture:

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment5/Screenshots/MAML/Model.png" width=500>

The below screenshot represents the model training:

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment5/Screenshots/MAML/MAML_Training.png" width=300>

The below screenshot represents the model training and test accuracies:

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment5/Screenshots/MAML/Accuracies.png" width=300>

The below screenshot represents the model predictions:

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment5/Screenshots/MAML/Predictions.png"  width=500>


## CMPE297_HW5_MMOE.ipynb

* The basic idea is to allow the model to figure out the extent of sharing th elower level features.
* Multi-gate Mixture-of-Experts (MMoE) learns to model task relationships from data. 
* **Dataset used:** https://archive.ics.uci.edu/ml/datasets/Census-Income+(KDD)

The below screenshot represents the model architecture:

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment5/Screenshots/MMOE/Model.png" width=500>

The below screenshot represents the last epoch statistics:

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment5/Screenshots/MMOE/LastEpoch.png" width=700>


## **Main References:**
* https://keras.io/examples/vision/reptile/
* https://www.analyticsvidhya.com/blog/2021/05/an-introduction-to-few-shot-learning/
* https://towardsdatascience.com/a-search-for-efficient-meta-learning-mamls-reptiles-and-related-species-e47b8fc454f2
* https://en.wikipedia.org/wiki/Multi-task_learning#:~:text=Multitask%20Learning%20is%20an%20approach,tasks%20as%20an%20inductive%20bias.&text=In%20the%20classification%20context%2C%20MTL,tasks%20by%20learning%20them%20jointly.
* https://towardsdatascience.com/multi-task-learning-with-multi-gate-mixture-of-experts-b46efac3268
* https://www.youtube.com/watch?v=Dweg47Tswxw


