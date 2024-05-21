# Apriori Algorithm

## Introduction

The Apriori Algorithm is a classic algorithm used in data mining for mining frequent itemsets and relevant association rules. This repository contains an implementation of the Apriori Algorithm in Python.

## Features

- Finds frequent itemsets from a given dataset.
- Generates strong association rules from the frequent itemsets.
- Supports customization of minimum support and confidence thresholds.
- Easy to use and integrate with other data processing pipelines.

## Getting Started

### Prerequisites

- Python 3.6 or higher
- Required Python libraries: `pandas`, `numpy`

### Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/apriori-algorithm.git
cd apriori-algorithm
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

## Usage
Prepare your dataset in a CSV file where each row represents a transaction and each column represents an item.

Import the apriori module and run the algorithm:
```python
from apriori import apriori

# Load your dataset
import pandas as pd
data = pd.read_csv('path_to_your_dataset.csv')

# Set your parameters
min_support = 0.5
min_confidence = 0.7

# Run Apriori Algorithm
frequent_itemsets, rules = apriori(data, min_support, min_confidence)

# Output the results
print("Frequent Itemsets:")
print(frequent_itemsets)

print("\nAssociation Rules:")
for rule in rules:
    print(rule)
```
## Example
Here's a small example of how to use the algorithm with a sample dataset:

```python
from apriori import apriori

# Sample dataset
data = pd.DataFrame({
    'Item1': [1, 1, 0, 1, 0],
    'Item2': [0, 1, 1, 0, 1],
    'Item3': [1, 1, 0, 0, 1],
    'Item4': [0, 1, 0, 1, 1]
})

min_support = 0.5
min_confidence = 0.7

frequent_itemsets, rules = apriori(data, min_support, min_confidence)

print("Frequent Itemsets:")
print(frequent_itemsets)

print("\nAssociation Rules:")
for rule in rules:
    print(rule)
```
## Output
The output consists of two parts:

Frequent Itemsets: List of itemsets that meet the minimum support threshold.
Association Rules: List of rules that meet the minimum confidence threshold, with their support, confidence, and lift values.
Contributing
Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgements
This implementation is inspired by various resources on data mining and machine learning.
Special thanks to the contributors and the open-source community.
