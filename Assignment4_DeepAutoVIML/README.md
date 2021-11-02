# HW4: Using Deep AutoVIML for various tasks based on Tabular, Text, and Image data.

deep_autoviml is a powerful deep learning library with the goal of making it easy for beginners to experts - to experiment with tensorflow.keras preprocessing pipelines and models using few lines of code.

* It can build models using tabular data, NLP and image datasets
* It can also handle time series data sets
* We can either allow deep_autoviml to automatically build a custom Tensorflow model for our usecase or use our own model of choice("bring your own model") to perform the tasks.
* It uses STORM/optuna tuner that quickly searches for the best hyperparameters for our model in fewer than 25 trials (specified as max_trials).

**Command for installing and importing deep auto VIML:**

```!pip install deep_autoviml --upgrade```

```from deep_autoviml import deep_autoviml as deepauto```


## CMPE297_HW4_Tabular.ipynb

Uses the churn dataset available at : https://raw.githubusercontent.com/srivatsan88/YouTubeLI/master/dataset/WA_Fn-UseC_-Telco-Customer-Churn.csv

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment4_DeepAutoVIML/Screenshots/Tabular/Churn_dataset.png" width=500>

Below screenshot shows how the deep auto VIML analyses the columns of the above dataset:

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment4_DeepAutoVIML/Screenshots/Tabular/Churn_Analysis_DeepAutoVIML.png" width=500>

The deep auto VIML finds the below hyperparameters to be the best amongst all the searches:

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment4_DeepAutoVIML/Screenshots/Tabular/BestHyperparameters_Churn.png" width=300>

The training and validation loss and accuracy curves are as follows:

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment4_DeepAutoVIML/Screenshots/Tabular/Churn_loss_acc.png" width=500>

The confusion matrices for training and validation are as follows:

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment4_DeepAutoVIML/Screenshots/Tabular/ConfusionMatrix_Churn.png" width=500>

**The following steps are happening:**

* It summarizes all the options we have specified.
* It loads the data
* Describes the columns of the data - which are numeric and which are categorical, tried to understand the vocab to understand what preprocessing is required.
* Performs preprocessing
* Recommends the number of layers if we want to customize it
* The storm tuner trains the keras model - for 10 trials, hyperparameters are tuned (Dropout, optimizer, number of layers in the model etc.)
* The best model is then picked.

**The average accuracy achieved by the model is 72% with the Survived='NO' class accuracy being 87% and 'YES' being 57%**

---------------
## CMPE297_HW4_Text.ipynb

Uses the twitter sentiment dataset available at : https://www.kaggle.com/arkhoshghalb/twitter-sentiment-analysis-hatred-speech

Below screenshot shows how the deep auto VIML analyses the columns of the above dataset:

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment4_DeepAutoVIML/Screenshots/Text/Tweet_analysis.png" width=500>

Below screenshot shows how the deep auto VIML analyses vocabulary size of input and the given size to create embeddings:

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment4_DeepAutoVIML/Screenshots/Text/Tweet_embedding.png" width=500>

The deep auto VIML finds the below hyperparameters to be the best amongst all the searches:

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment4_DeepAutoVIML/Screenshots/Text/BestHyperparameters_Tweet.png" width=300>

The training and validation loss and accuracy curves are as follows:

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment4_DeepAutoVIML/Screenshots/Text/Tweet_loss_acc.png" width=500>

The confusion matrices for training and validation are as follows:

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment4_DeepAutoVIML/Screenshots/Text/Tweet_confusionMatrix.png" width=500>

**The following steps are happening:**

* It summarizes all the options we have specified.
* It loads the data
* The deep autoVIML finds that there is an NLP column automatically and chooses an embedding size of 50. The original vocabulary size of the input was 409623 and its lowered down to 50 which was the inout.
* Goes into building a model and runs for the given max_trial times.
* The storm tuner trains the keras model - for 15 trials, hyperparameters are tuned (Dropout, optimizer, number of layers in the model etc.)
* The best model is then picked.

**The average accuracy achieved by the model is 85% with the Class=0 class accuracy being 92% and Class=1 being 37%**

---------------
## CMPE297_HW4_Image.ipynb

Uses the rock paper scissors dataset available at : https://www.kaggle.com/drgfreeman/rockpaperscissors?select=README_rpc-cv-images.txt

Model input and model training by deep auto VIML are as follows:

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment4_DeepAutoVIML/Screenshots/Images/ModelTraining_rockpaper.png" width=500>

Model architecture as chosen by deep auto VIML as follows:

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment4_DeepAutoVIML/Screenshots/Images/ModelArchi_rockpaper.png" width=500>

The training and validation loss and accuracy curves are as follows:

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment4_DeepAutoVIML/Screenshots/Images/rockpaperscissor_loss_acc.png" width=500>

Predictions served by the model created by our deep auto VIML:

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment4_DeepAutoVIML/Screenshots/Images/Predictions_rockpaper.png" width=500>

**Points to note:**

* The above process is using a pretrained model for the defined task - mobile vnet model.
* Scaling of the images is also automatically handled










