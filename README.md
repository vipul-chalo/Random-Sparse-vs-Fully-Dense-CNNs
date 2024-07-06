# 📈 Random Sparse or Fully Connected Layers in CNN

## ✏️ Introduction

Personal project to explore sparsity in CNNs and their affect on model performance.

Using Deep Learning CNN model to classify 10 images into their classes. The work is based on the CIFAR-10 dataset from [Alex Krizhevsky's Home Page at University of Toronto](https://www.cs.toronto.edu/~kriz/cifar.html).

I performed the image classification on 2 different models with similar structure. After multiple covolutions, dropout, batchnormalization, and maxpooling layers, the difference lies in the final structure.

Run 1:
     The dense model consists 2 dense layers with 512 and 128 units before the final predictions. 
     The sparse model consists 2 sparse layers with 512 and 128 units before the final predictions.

Run 2:
     The dense model consists 4 dense layers with 2048, 512, 128, and 32 units before the final predictions. 
     The sparse model consists 4 sparse layers with 2048, 512, 128, and 32 units before the final predictions.

See the included plots for a summary and conclusion of the work.

## 📦 Installation

The following packages are required to run the code:

- [Numpy](https://numpy.org/)
- [Matplotlib](https://matplotlib.org/)
- [sklearn](https://scikit-learn.org/stable/)
- [TensorFlow](https://www.tensorflow.org/)

You should also have some sort of Python environment manager installed, such as [Anaconda](https://www.anaconda.com/).

## 🏗️ Included Models:

1. Densely Connected CNN:
   Run 1: In the fully connected CNN, the model had a total of 1,403,498 trainable parameters.
   Run 2: In the fully connected CNN, the model had a total of 21,044,682 trainable parameters.

2. Sparsely Connected CNN:
   Run 1: In the sparsely connected CNN, the model had a total of 353,386 trainable parameters, which is around 74.82% less trainable parameters than the dense model.
   Run 2: In the sparsely connected CNN, the model had a total of 3,323,818 trainable parameters, which is around 84.21% less trainable parameters than the dense model.

## 🎯 Results:

RUN 1 Final Results:
1. Densely Connected CNN:
   1. Final Training Accuracy - 0.8205
   2. Final Training Loss - 0.5181
   3. Final Validation Accuracy - 0.8552
   4. Final Validation Loss - 0.4342
   5. Testing Accuracy - 0.8658
   6. Testing Loss - 0.4207
  
2. Sparsely Connected CNN:
   1. Final Training Accuracy - 0.7938
   2. Final Training Loss - 0.5902
   3. Final Validation Accuracy - 0.8406
   4. Final Validation Loss - 0.4837
   5. Testing Accuracy - 0.8400
   6. Testing Loss - 0.4804
  
RUN 2 Best Epoch Results:
1. Densely Connected CNN:
   1. Training Accuracy - 0.8926
   2. Training Loss - 0.3214
   3. Validation Accuracy - 0.8884
   4. Validation Loss - 0.3582
   5. Testing Accuracy - 0.8858
   6. Testing Loss - 0.3541
  
2. Sparsely Connected CNN:
   1. Training Accuracy - 0.8796
   2. Training Loss - 0.3475
   3. Validation Accuracy - 0.8828
   4. Validation Loss - 0.3727
   5. Testing Accuracy - 0.8456
   6. Testing Loss - 0.4677
  
The overall results indicate that random sparse CNN performs almost on-par with the fully dense CNN even with significantly less trainable parameters. It is visible through the accuracy plots that the slope for the dense models is slightly higher than the sparse models, which signifies that if we were to keep training for more epochs, the gap in accuracy might have increased. Nonetheless, sparse models' little less accurate results seem insignificant when compared to 75% and 84% less parameters. 
