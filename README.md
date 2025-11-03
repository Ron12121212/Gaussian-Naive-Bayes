# Gaussian Naive Bayes Image Classifier

A Python-based machine learning project that implements a **Gaussian Naive Bayes (GNB)** classifier for grayscale image classification.  
The system is built from scratch without using built-in classifiers, providing hands-on experience with model development, parameter estimation, and performance evaluation.

# Project Overview

This project loads grayscale image datasets from `.pkl` files and classifies them into one of five fashion-related classes using Gaussian Naive Bayes.  
It covers data preparation, visualization, parameter estimation, classification, and performance metrics using training and testing sets.

# Dataset

The data is loaded from two serialized files:

- `TrainData.pkl` – training images and labels
- `TestData.pkl` – test images and labels

Each image is a 2D grayscale image, and labels are integers from 0 to 4 representing:

```
0: T-shirt/top
1: Trouser
2: Coat
3: Sandal
4: Ankle boot
```

# Key Features

- Data loading from `.pkl` files using `pickle`
- Image reshaping and visualization using `matplotlib`
- Label-to-name mapping for better interpretability
- Gaussian Naive Bayes classifier implemented from scratch:
  - Estimation of class priors, feature means, and covariances
  - Multivariate Gaussian likelihood computation
- Evaluation metrics:
  - Accuracy score using `sklearn.metrics`
  - Confusion matrix for training and test sets
- Visualization of one example per class and class-mean images

# Requirements

- Python 3.x
- NumPy
- Matplotlib
- scikit-learn

Install dependencies using:

```
pip install numpy matplotlib scikit-learn
```

# How to Run

1. Make sure `TrainData.pkl` and `TestData.pkl` are in the same directory as the script.
2. Run the Python file:

```bash
python your_script_name.py
```

3. You will see:
   - Visualizations of training/test samples and class-mean images
   - Accuracy scores for both training and test sets
   - Confusion matrices printed to the console

# File Structure

```
project-root/
├── your_script_name.py
├── TrainData.pkl
├── TestData.pkl
```

# Notes

- This implementation assumes full-rank covariance matrices. In some datasets, regularization might be required.
- Accuracy depends heavily on data quality and size of the dataset.
- All math operations are vectorized for performance.

# License

This project is released for educational and academic use.  
You are free to reuse, modify, and extend this code for personal or non-commercial use.

© 2025 Ron Haba  
All rights reserved.
