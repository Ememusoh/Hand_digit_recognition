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

 ## Prerequisites & Installation
 1. Clone the repository
 2. Create and activate a virtual environment (optional but recommended
 3. Install dependencies

 ## Usage
Run the Jupyter Notebook
Navigate to notebooks/model-training.ipynb to see the step-by-step process:

Load MNIST data.
Perform PCA (tune the number of components).
Train and evaluate the Random Forest Classifier.
Hyperparameter Tuning
You can adjust hyperparameters of the Random Forest (e.g., n_estimators, max_depth) in the notebook or in src/random_forest.py.

Visualizing PCA
PCA can help visualize data in 2D or 3D. You can see the variance ratio plot in images/pca_variance_plot.png (placeholder example):

## Results
Once the model is trained, you can evaluate its performance using metrics like accuracy, precision, recall,
Digit Predicted →  0    1    2    ...   9
        0         578   0    1    ...   0
        1          0   660   2    ...   0
        2          0    1   568   ...   3
        ...
        9          1    0    0    ...  570

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Fork the project.
Create a new branch for your feature: git checkout -b feature/your-feature
Commit your changes: git commit -m 'Add some feature'
Push to the branch: git push origin feature/your-feature
Open a Pull Request.


## License
This project is licensed under the MIT License. Feel free to use and modify the code in your own projects.
