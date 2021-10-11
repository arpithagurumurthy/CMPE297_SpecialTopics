# Perceiver IO model implementation

A General Architecture for Structured Inputs & Outputs by Deepmind

* It is considered as a generalized architecture that solves quadratic time and space complexity with transformers which occurs due to attention mechanism.
* It is a generalization of Perceiver to handle arbitrary outputs in addition to arbitrary inputs. 
* The original Perceiver only produced a single classification label. 
* In addition to classification labels, Perceiver IO can produce (for example) language, optical flow, and multimodal videos with audio. 
* This is done using the same building blocks as the original Perceiver. 
* The computational complexity of Perceiver IO is linear in the input and output size and the bulk of the processing occurs in the latent space, allowing us to process inputs and outputs that are much larger than can be handled by standard Transformers. 
* This means, for example, Perceiver IO can do BERT-style masked language modeling directly using bytes instead of tokenized inputs.

Following tasks have been implemented:

* Image classication: 
**Model:** Imagenet base and path for the trained weights of the model -

```CHECKPOINT_URLS = {
    'conv_preprocessing': 'https://storage.googleapis.com/perceiver_io/imagenet_conv_preprocessing.pystate',
    'fourier_position_encoding': 'https://storage.googleapis.com/perceiver_io/imagenet_fourier_position_encoding.pystate',
    'learned_position_encoding': 'https://storage.googleapis.com/perceiver_io/imagenet_learned_position_encoding.pystate'}
```

**Results: 

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment2_Perceiver/Part2_PerceiverIO/golden_retriever.png" width = 500>
We can see the top 5 labels with the probabilities displayed with the top probality for golden retriever precisely.

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment2_Perceiver/Part2_PerceiverIO/pomegranate.png" width = 500>
We can see the top 5 labels with the probabilities displayed with the top probality for pomegranate precisely.


* Masked language modeling
* Optical flow
* Video autoencoding

## **References**
* https://github.com/2796gaurav/code_examples/blob/main/Perceiver/Perceiver_imagenet_classification.ipynb
* https://www.apache.org/licenses/LICENSE-2.0


