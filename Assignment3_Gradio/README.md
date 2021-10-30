# Fientuning Bert for various NLP tasks, integrating Gradio and Tensorboard

BERT is one of the most popular transformer-based models

**Model finetuning**

* BERT (Bidirectional Encoder Representations from Transformers) is a huge neural network architecture, with a huge number of parameters, that can range from 100 million to over 300 million. So, training a BERT model from scratch on a small dataset would result in overfitting.
* It is better to use a pre-trained BERT model that is trained on a huge dataset, as a starting point. We can further train the model on a smaller dataset. This is known as model fine-tuning.

## **CMPE297_HW3_SpamClassification.ipynb** 
Implements spam classification for messages using BERT finetuning.

The below screenshot shows the prediction of the finetuned Bert model on Gradio:

* **Model classifying the message as spam**
<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment3_Gradio/Screenshots/Spam.png">

* **Model classifying the message as spam**
<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment3_Gradio/Screenshots/Non%20Spam.png">

* **Tensorboard logs for training loss:**
<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment3_Gradio/Screenshots/TensorBoard/SpamClassn_TB.png">

* **Tensorboard logs for validation loss:**
<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment3_Gradio/Screenshots/TensorBoard/SpamClassn_TB_Val.png">

## **CMPE297_HW3_TopicModeling.ipynb** 

Implements Contextualized Topic Models - CTMs are a family of topic models that combine the expressive power of BERT embeddings with the usupervised capabilities of topic models to get topics out of documents.

The below screenshot shows the prediction of the finetuned CTM model on Gradio:

* **Model serving predictions for topic modeling:**
<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment3_Gradio/Screenshots/Topic_Modeling.png">

* **Tensorboard logs for topic modeling:**
<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment3_Gradio/Screenshots/TensorBoard/TopicModeling_TB.png">




## **References:**
* https://www.analyticsvidhya.com/blog/2020/07/transfer-learning-for-nlp-fine-tuning-bert-for-text-classification/
