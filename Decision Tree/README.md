# Overview
This Jupyter Notebook contains an implementation of the ID3 Decision Tree algorithm to classify data using different heuristics: Information Gain (Entropy), Majority Error, and Gini Index. The notebook processes a dataset (train.csv and test.csv), converts numerical columns to binary, and applies the decision tree algorithm to predict the target label.

# Files
train.csv: Training dataset file (without headers).
test.csv: Testing dataset file (without headers).

# How to Run the Code
Load the Jupyter Notebook and execute all cells sequentially.
# The code will:
Load the train and test datasets.
Convert numerical columns into binary (0/1) based on the median of each column.
Implement and execute the ID3 Decision Tree using three heuristics (Information Gain, Majority Error, Gini Index).

# Parameters
heuristic: You can choose between:
  information_gain: Uses Entropy for the decision tree split.
  majority_error: Uses the majority error rate for the split.
  gini_index: Uses the Gini Index for the split.
max_depth: Defines the maximum depth for the decision tree. The range is from 1 to 16 in the current implementation.

# Results
The notebook will display a DataFrame showing:
  Heuristic used (Heuristic),
  Maximum tree depth (Max Depth),
  Training error (Train Error),
  Testing error (Test Error).

# Example output:
Heuristic	Max Depth	Train Error	Test Error
information_gain	1	0.15	0.17
gini_index	2	0.12	0.15

# Customizing
The code can be modified to:
  Adjust the heuristic function by selecting a different option in the heuristics dictionary.
  Change the maximum depth for the decision tree by passing a different max_depth value to DecisionTreeID3Modified.
