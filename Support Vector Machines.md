# Support Vector Machine

[TOC]

------

## Generation (optional)

The timeline of generation of SVM can be seen in Fig. x.

## Introduction

Support vector machine (SVM) is a class of powerful tools, becoming increasingly siginificant in the field of data mining, classification, pattern recognition and optimization etc. Also, it's typically classed as "machine learning" referring to supervised learning.

There are two main learning keys in SVM:

- **Computational learning theory**

  Statistical learning theory models this as a function estimation problem.

- **Learning functions - "kernel functions"**

  Linear, nonlinear, polynomial, radial basis function (RBF), and sigmoid etc.

## Motivation

### General part

The original issue to be addressed is one of the **supervised binary classification**. The aim is to separate some kind of complex data into different categories. For $k$ different classes task, we can adopt *one versus all (OvA)* or *one versus one (AvA)* principle (in R code use).

### Engineering part

Examples

## Key Indications

### Computational learning theory

- **Maximum Margin**

- **Support Vectors**

  **Support Vectors** are those datapoints which the margin pushes up against.

  In short, Support Vectors:

  - intuitively the co-ordinates of individual observations. 
  - data points that lie closest to the hyperplane, that is, decision surface.
  - data points most difficult to classify.
  - the critical elements of a data set since they would alter the position of the dividing hyperplane (added or removed).

  ***? we can demonstrate that the optimal hyperplane stems from the function class with the lowest "capacity" (VC dimension)*** Vapnik-Chervonenkis (VC)

- **Large-margin Decision Boundary**

- **Maximal margin hyperplane (MMH)**

  It is the separating hyperplane that is farthest from any training observations, and is thus "optimal".

- **Support Vector Classifiers (SVC) or Soft Margin Classifier** 

  An SVC allows some points to be on the incorrect side of the margin (or hyperplane) which can help to avoid over-fitting problem and improve the model's robustness in some degree. Hence it provides a "soft" separation.

### Learning functions - "kernel functions"

- 

## Interpretation

### Mathmetical interpretation

### Geometrical interpretation







## Goodnesses & Weaknesses

### Goodness

**High Dimensinality**: SVM is an effective tool in addressing high-dimensional problem, which is particularly applcable to classification and sentiment analysis with high-dimension.

**Memory Efficiency**: Just the points in the subset of training points are stored in memory or calculated when making decisions.

**Versatility**: The separation of class is usually highly non-linear. Therefore, the ability to apply new kernels allows substantial flexibility for the decision surfaces, leading to greater classification performance.

### Weakness

**Sensitive to Noise**: A fairly small number of misclassified points may dramatically decrease the performance of classification.

**Kernel Parameter Selection**: SVMs are quite sensitive to the choice of the kernel paramters. *For instance, in situations where the number of features for each observation exceeds the numebr of training data samples, SVMs perform poorly to some extent.* 

**Non-Probailistic**: There is *no direct probabilistic interpretation* for group membership since the classifier works via placing observations above or below the decision boundary (or hyperplane).

## Challenges

- **Choice of kernel**
  - Gaussian or polynomial kernel is usual default
  - If ineffective, more elaborate kernels are needed

- **Choice of kernel parameters**
  - e.g. $\sigma$ in Gaussian kernel
  - $\sigma$ is the distance between closest points with different classifications
  - in the absence of reliable criteria, applications rely on the use of a validation set or cross-validation ro set such parameters

- **Optimization criterion - Hard margin vs. Soft margin**

## Code practice
