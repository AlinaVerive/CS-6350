# Perceptron Algorithms

This repository contains implementations of three Perceptron algorithms for classifying banknotes as genuine or forged based on image features. The dataset is derived from images of banknotes, and features are extracted using Wavelet Transform. The goal is to compare the performance of the **Standard Perceptron**, **Voted Perceptron**, and **Average Perceptron** algorithms.

## Dataset
- **`train.csv`**: Training dataset (872 examples)
- **`test.csv`**: Testing dataset (500 examples)
- **`data-desc`**: Description file outlining the features and label format

The dataset includes:
1. **Variance** of the Wavelet Transformed image
2. **Skewness** of the Wavelet Transformed image
3. **Curtosis** of the Wavelet Transformed image
4. **Entropy** of the image
5. **Label** (0 for forged, 1 for genuine)

The labels are converted to -1 and +1 for compatibility with the Perceptron algorithms.

## Perceptron Algorithms

### Standard Perceptron
The **Standard Perceptron** updates the weight vector each time an example is misclassified. After training, the learned weight vector is used to classify test examples.

### Voted Perceptron
The **Voted Perceptron** algorithm keeps a list of distinct weight vectors, each associated with a count of the correctly classified examples it achieved before the next update. During testing, each test example is classified based on the weighted vote from these weight vectors.

### Average Perceptron
The **Average Perceptron** keeps a running average of the weight vector across all updates. This averaged weight vector is then used for classification, which generally improves stability and reduces variance.

## Usage

1. **Load Data**: Ensure the `train.csv` and `test.csv` files are in the same directory as the script.
2. **Run the Script**: Execute it.

The script will load the dataset, train each Perceptron model, and report the learned weight vectors and test error rates.

## Output

The script will output:
- **Learned weight vector** for each algorithm
- **Average test error** on the `test.csv` dataset for each algorithm
- **Comparison** of test errors for the three Perceptron methods

Example output:
```plaintext
Standard Perceptron Weights: [...]
Standard Perceptron Test Error: 0.05

Voted Perceptron Weights and Counts: [([...], count), ...]
Voted Perceptron Test Error: 0.04

Average Perceptron Weights: [...]
Average Perceptron Test Error: 0.03

Comparison of Errors:
Standard Perceptron Test Error: 0.05
Voted Perceptron Test Error: 0.04
Average Perceptron Test Error: 0.03
```
