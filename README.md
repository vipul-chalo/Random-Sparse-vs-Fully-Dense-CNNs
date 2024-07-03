# 📈 Random Sparse or Fully Connected Layers in CNN

## ✏️ Introduction

Personal project to explore sparsity in CNNs and their affect on model performance.

Using Deep Learning CNN model to classify 10 images into their classes. Based on the CIFAR-10 dataset from [Alex Krizhevsky's Home Page at University of Toronto](https://www.cs.toronto.edu/~kriz/cifar.html).

I performed the image classification on 2 different models with similar structure. After multiple covolutions, dropout, batchnormalization, and maxpooling layers, the difference lies in the final structure. The dense model consists 2 dense layers with 512 and 128 units before the final predictions. The sparse model consists 2 sparse layers with 512 and 128 units before the final predictions.

See the `Final Presentation.pdf` file for a summary and conclusion of our work.

## 📦 Installation

The following packages are required to run the code:

- [Pandas](https://pandas.pydata.org/)
- [Numpy](https://numpy.org/)
- [Matplotlib](https://matplotlib.org/)
- [sklearn](https://scikit-learn.org/stable/)
- [seaborn](https://seaborn.pydata.org/)

You should also have some sort of Python environment manager installed, such as [Anaconda](https://www.anaconda.com/).

## 🎯 Included Models:

1. Logistic Regression
2. Linear Kernel SVM
3. 2nd Degree Polynomial Kernel SVM
4. 3rd Degree Polynomial Kernel SVM
5. 4th Degree Polynomial Kernel SVM

## 🏗️ Four datasets:

### 1. The Whole Dataset

Run `whole_data_run.ipynb` file to get results of all five models on the whole non-reduced dataset.

### 2. Feature Mean Value Reduced Dataset

In this approach, we separated the training dataset into two `3000 x 5000` datasets based on their labels either `1` or `-1`. Then we calculated mean across the features to get two `1 x 5000` datasets that stored the average values. Afterwards, we calculated the differene between these mean values stored in the two datasets individually for each feature. Then filtered down our features using the absolute value of this difference to be at least `50`.

Run `feature_mean_reduced_data_run.ipynb` file to gain a better understanding of our approach and to get results of all five models on this reduced dataset.

### 3. Correlation & Multi-Collinearity Reduced Dataset

Here we calculated correlation of each feature to the target value and kept a feature only if it was at least in 15% correlation with the target.
Then we calculated Variance Inflation Factor of the remaining dataset and kept a feature only if it had VIF less than 10.

Run `correlation_multicollinearity_reduced_data_run.ipynb` file to gain a better understanding of our approach and to get results of all five models on this reduced dataset.

### 4. Principal Component Analysis Reduced Dataset

We performed PCA on our dataset and reduced the features to principal components capturing at least 85% variability of the dataset.

Run `PCA_reduced_data_run.ipynb` file to gain a better understanding of our approach and to get results of all five models on this reduced dataset.
