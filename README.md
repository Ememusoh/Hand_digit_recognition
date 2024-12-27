# MNIST Handwritten Digit Recognizer

A machine learning project that uses **Principal Component Analysis (PCA)** for dimensionality reduction and a **Random Forest Classifier** to recognize handwritten digits from the MNIST dataset.

---

## Table of Contents
1. [Overview](#overview)
2. [Project Structure](#project-structure)
3. [Data](#data)
4. [Prerequisites & Installation](#prerequisites--installation)
5. [Usage](#usage)
6. [Results](#results)
7. [Contributing](#contributing)
8. [License](#license)

---

## Overview
The MNIST dataset contains 70,000 grayscale images of handwritten digits (0–9), each of size 28x28 pixels. This project demonstrates how to:
1. Load and preprocess the data (flattening images and splitting into train/test sets).
2. Apply **PCA** to reduce the dimensionality of the feature space.
3. Train a **Random Forest Classifier** on the transformed data.
4. Evaluate the performance of the model.

        +-----------------------+       +-----------------------+
        | MNIST Data (28x28)   |       | Random Forest         |
        +-----------------------+       +-----------+-----------+
                    |                               ^
                    v                               |
             +--------------+                       |
             |  PCA (dim)   |                       |
             |    reduce    |-----------------------+
             +--------------+
*(Above: High-level flow of the pipeline.)*

---

## Project Structure


---

## Data
The MNIST dataset can be downloaded from [MNIST Official Website](http://yann.lecun.com/exdb/mnist/) or via machine learning libraries (e.g., `sklearn.datasets`). Typically, it is loaded with:
```python
from sklearn.datasets import fetch_openml

mnist = fetch_openml('mnist_784', version=1)
X, y = mnist.data, mnist.target

![Sample MNIST Digits](sample_mnist_digits.png)