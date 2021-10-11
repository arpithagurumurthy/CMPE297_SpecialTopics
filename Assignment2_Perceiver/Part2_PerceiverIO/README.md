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

## **Image classication:**

**Model:** Imagenet base and path for the trained weights of the model -

```CHECKPOINT_URLS = {
    'conv_preprocessing': 'https://storage.googleapis.com/perceiver_io/imagenet_conv_preprocessing.pystate',
    'fourier_position_encoding': 'https://storage.googleapis.com/perceiver_io/imagenet_fourier_position_encoding.pystate',
    'learned_position_encoding': 'https://storage.googleapis.com/perceiver_io/imagenet_learned_position_encoding.pystate'}
```

**Results:**

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment2_Perceiver/Part2_PerceiverIO/golden_retriever.png" width = 500>
We can see the top 5 labels with the probabilities displayed with the top probality for golden retriever precisely.

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment2_Perceiver/Part2_PerceiverIO/pomegranate.png" width = 500>
We can see the top 5 labels with the probabilities displayed with the top probality for pomegranate precisely.


## **Masked language modeling:**

It involves - input a sentence (with masked words) into the model and optimizing the weights inside model to output the the words missing or masked.

**Results:**

* input sentence: "This is an incomplete sentence where some words are missing."
* After masking the work 'missing': This is an incomplete sentence where some words are
* Output:
Greedy predictions:
[ 38 115 111 121 121 111 116 109  52]

Predicted string:
 missing.
***We can see that the model predicted the missing word to be 'missing'.***


## Optical flow:

Optical flow or optic flow is the pattern of apparent motion of objects, surfaces, and edges in a visual scene caused by the relative motion between an observer and a scene. Optical flow can also be defined as the distribution of apparent velocities of movement of brightness pattern in an image.

**Dataset:** Sintel dataset
A data set for the evaluation of optical flow derived from the open source 3D animated short film, Sintel.

**Model:** Path for the trained weights of the model -
https://storage.googleapis.com/perceiver_io/optical_flow_checkpoint.pystate

**Results:**

<img src="https://github.com/arpithagurumurthy/CMPE297_SpecialTopics/blob/main/Assignment2_Perceiver/Part2_PerceiverIO/pomegranate.png" width = 500>

Optical flow - the motion of individual pixels on the image plane. It often serves as a good approximation of the true physical motion projected onto the image plane.


* Video autoencoding

## **References**
* https://medium.com/analytics-vidhya/perceiver-io-a-general-architecture-for-structured-inputs-outputs-4ad669315e7f
* https://github.com/2796gaurav/code_examples/blob/main/Perceiver/Perceiver_imagenet_classification.ipynb
* https://www.apache.org/licenses/LICENSE-2.0
* https://deepmind.com/research/open-source/perceiver-IO
* https://en.wikipedia.org/wiki/Optical_flow#:~:text=Optical%20flow%20or%20optic%20flow,brightness%20pattern%20in%20an%20image.
* http://sintel.is.tue.mpg.de/


