# Image Caption Generator

Image Caption Generator is a machine learning model that can generate meaningful textual descriptions for a given image.

# Table of Contents

- [Image Caption Generator](#image-caption-generator)
- [Table of Contents](#table-of-contents)
- [Brief Overview](#brief-overview)
- [Installation](#installation)
- [Data Sources](#data-sources)
- [Model](#model)

# Brief Overview

[(Back to top)](#table-of-contents)

This project involved building a model that can generate meaningful textual descriptions for given input images. To start, we gathered a dataset of images and their associated captions. Once we have completed the data collection process, we proceeded to build a model using Convolutional Nueral Networks (CNN) and Recurrent Nueral Networks (RNN) in combination. CNNs were used to extract meaningful features from the input images, while RNNs, specifically Long Short-Term Memory (LSTM) networks, were employed to generate captions based on the extracted features.

# Installation

[(Back to top)](#table-of-contents)

Open Git Bash and change the directory to the location where the repository is to be cloned. Then, type the following commands.

```shell
  git init
```

```shell
  git clone https://github.com/kashish-a/Image-to-Caption-Generator.git
```

Now, install the requirements using the following command.

```shell
   pip install -r requirements.txt
```

To access or use the application, open a terminal in the cloned repository folder and run the following command.

```shell
  streamlit run deployment.py
```

Finally, browse the link provided in your browser.

# Data Sources

[(Back to top)](#table-of-contents)

The dataset used was Flickr 8k dataset. It consists of 8,000 images that are each paired with five different captions which provide clear descriptions of the salient entities and events. The images were chosen from six different Flickr groups, and tend not to contain any well-known people or locations, but were manually selected to depict a variety of scenes and situations.

- Flickr 8k Dataset ( [Link](https://www.kaggle.com/datasets/adityajn105/flickr8k) )

# Model

[(Back to top)](#table-of-contents)

The model has two inputs - image features and captions data sequences. Model was trained using LSTMs and the ouput was the probability of each word in the vocabulary. The output layer had activation `softmax`.

Thus, for generating captions for any image, the word was found for the index with the maximum probability and it was added to the caption. If the predicted word was `end`, the caption ended.

> Model architecture and model summary are uploaded.
