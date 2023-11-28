# Stable-Diffusion---Image-to-Prompt
## Problem Statement
The popularity of text-to-image models has spurned an entirely new field of prompt engineering. Part art and part unsettled science, ML practitioners and researchers are rapidly grappling with understanding the relationships between prompts and the images they generate. In this project, we aim to reverse the typical direction of a generative text-to-image model: instead of generating an image from a text prompt, can you create a model which can predict the text prompt given a generated image? You will make predictions on a dataset containing a wide variety of (prompt, image) pairs generated by Stable Diffusion 2.0 to understand how reversible the latent relationship is.

## Methodology
I have used the encoder-decoder model to create our image caption generator, with the encoder as a CNN network and the decoder as an LSTM network, and used <a href="https://www.kaggle.com/datasets/adityajn105/flickr8k">Flickr8k dataset</a> for training.<br>

### Encoder:
For feature extraction, the model uses ResNet50 pre-trained on ImageNet dataset (which needs an image input of size 224*224*3) where the features of the image are extracted just before the last layer of classification. Another dense layer is added and converted to get a vector of length 2048.
### Decoder:
I have used a normal RNN(LSTM) as decoder.

### Model Architecture:
<a href="https://ibb.co/pXMdGKk"><img src="https://i.ibb.co/C0YQN9S/model.png" alt="model" border="0"></a><br /> </a><br />


## References
  - Show and Tell: A Neural Image Caption Generator  (https://arxiv.org/abs/1411.4555) <br/>
  - Tensorflow Tutorials<br/>
  This project is done under the guidance of Vision And Language Group @IIT Roorkee

## Contributers
  <a href="https://github.com/praffulv-225">Prafful Varshney</a><br/>
