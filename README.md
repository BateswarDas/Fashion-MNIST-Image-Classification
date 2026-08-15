# Fashion-MNIST Image Classification Using a Neural Network
Deep learning-based image classification using a neural network and the Fashion-MNIST datasets.

## Overview

This project implements a deep-learning-based image classification workflow using the **Fashion-MNIST** dataset and **TensorFlow/Keras**.

The objective is to develop a neural network capable of classifying 28 × 28 grayscale images of clothing and footwear into 10 apparel categories. The workflow includes data loading, image visualization, pixel normalization, label encoding, neural-network development, model training, evaluation, prediction, training-monitoring, and model saving/restoration.

## Dataset

The **Fashion-MNIST** dataset contains 70,000 grayscale images of fashion products:

* **60,000 training images**
* **10,000 test images**
* Image dimensions: **28 × 28 pixels**
* Number of classes: **10**
* Pixel values: **0–255**, normalized to **0–1** before model training

The original dataset is provided by Zalando Research:

[Zalando Research — Fashion-MNIST](https://github.com/zalandoresearch/fashion-mnist)

### Classes

| Label | Class       | Description          |
| ----: | ----------- | -------------------- |
|     0 | T-shirt/top | Short-sleeved top    |
|     1 | Trouser     | Pants                |
|     2 | Pullover    | Long-sleeved sweater |
|     3 | Dress       | One-piece dress      |
|     4 | Coat        | Overcoat or jacket   |
|     5 | Sandal      | Open shoe            |
|     6 | Shirt       | Button-down shirt    |
|     7 | Sneaker     | Sports shoe          |
|     8 | Bag         | Handbag or tote      |
|     9 | Ankle boot  | Boot or shoe         |

## Methodology

The workflow consists of the following stages:

### 1. Data Loading

The Fashion-MNIST dataset is loaded using the TensorFlow/Keras dataset API.

### 2. Image Preprocessing

The 28 × 28 grayscale images are normalized by dividing pixel values by 255, converting the original 0–255 range to a 0–1 range.

The categorical labels are converted to one-hot encoded vectors for multi-class classification.

### 3. Neural Network Architecture

A fully connected feed-forward neural network is developed using Keras Sequential API.

The architecture consists of:

| Layer   | Configuration           |
| ------- | ----------------------- |
| Input   | 28 × 28 grayscale image |
| Flatten | 28 × 28 → 784 features  |
| Dense   | 128 neurons, ReLU       |
| Dense   | 64 neurons, ReLU        |
| Output  | 10 neurons, Softmax     |

The model contains **109,386 trainable parameters**.

### 4. Model Compilation

The model is compiled using:

* **Optimizer:** Adam
* **Loss function:** Categorical Cross-Entropy
* **Evaluation metric:** Accuracy

### 5. Model Training

The neural network is trained for:

* **Epochs:** 10
* **Batch size:** 64

Training and evaluation performance are monitored using TensorBoard.

### 6. Model Evaluation

Model performance is evaluated on the Fashion-MNIST test dataset. Training and test/validation accuracy and loss are also visualized to examine model learning behaviour.

### 7. Prediction

The trained model is used to predict apparel classes for previously unseen test images.

### 8. Model Saving and Restoration

The trained Keras model is saved in `.keras` format and subsequently loaded to verify model restoration and consistency of the stored weights.

## Results

After 10 training epochs, the model achieved:

* **Training accuracy:** approximately 91.13%
* **Test accuracy:** **88.71%**
* **Test loss:** approximately 0.337

The results demonstrate that a relatively simple fully connected neural network can learn useful representations from the Fashion-MNIST image data and perform multi-class apparel classification.

## Technologies

* **Python**
* **TensorFlow**
* **Keras**
* **NumPy**
* **Matplotlib**
* **TensorBoard**
* Deep Learning
* Neural Networks
* Image Classification

## Repository Contents

```text
Fashion-MNIST-Deep-Learning-Classification/
│
├── README.md
└── Fashion_MNIST_Classification.ipynb
```

## Reproducibility

The complete analysis and modelling workflow is provided in the Jupyter Notebook.

The notebook can be executed in a Python environment with TensorFlow/Keras and the required supporting libraries installed. The Fashion-MNIST dataset can be loaded directly through the TensorFlow/Keras dataset API.

## Author

**Bateswark Das**

This repository was developed as part of a data science/deep-learning coursework project to explore neural-network-based image classification.

Please acknowledge the author when reusing or adapting the code or analysis.
