# Fashion-MNIST Classification Using Autoencoder Network
## Overview
This project involves constructing an Autoencoder network using dense layers and then solving a classification problem on the Fashion-MNIST dataset. The Autoencoder is used to learn an efficient representation of the input data, which is subsequently fed into a classifier to predict the clothing item labels.
## Dataset
The [Fashion-MNIST dataset](https://github.com/zalandoresearch/fashion-mnist) is a widely used dataset consisting of 70,000 grayscale images in 10 categories. Each image is 28x28 pixels and belongs to one of the following classes:
- T-shirt/top
- Trouser
- Pullover
- Dress
- Coat
- Sandal
- Shirt
- Sneaker
- Bag
- Boot
The dataset is split into:
- **Training set**: 60,000 images
- **Test set**: 10,000 images
## Objectives
1. **Autoencoder Construction**:
   - Building an Autoencoder using dense layers.
   - Train the Autoencoder on the Fashion-MNIST dataset to learn a compressed representation of the input data.
3. **Classification**:
   - Using the encoded representations from the Autoencoder as input features for a classification model.
   - Implementing a classification network using dense layers.
   - Training the classification model on the encoded representations.
   - Evaluating the model’s performance using accuracy and loss metrics.
## Architecture
### Autoencoder
- **Encoder**:
    - Input layer: 784 units (flattened 28x28 image).
    - Several hidden dense layers with decreasing number of units.
    - Bottleneck layer: Encodes the image into a lower-dimensional space.
- **Decoder**:
    - Several hidden dense layers with increasing number of units.
    - Output layer: 784 units, reshaped back into the original 28x28 image.
### Classifier
- **Input Layer**: Takes the encoded representations (from the bottleneck layer).
- **Hidden Layers**: Dense layers for feature extraction and classification.
- **Output Layer**: 10 units with softmax activation for multi-class classification.
