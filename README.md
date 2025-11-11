Tumaini Micheni 933

 Overview

This project provides a simple demonstration of Association Rule Mining in Python using the mlxtend library.
It showcases how to identify relationships between items in transaction data (e.g., items commonly purchased together) using the Apriori algorithm and generate meaningful association rules based on support, confidence, and lift metrics.

 Key Concepts

Association Rule Mining: A machine learning technique that finds hidden relationships between variables in large datasets.

Apriori Algorithm: Identifies frequent itemsets in transaction data.

Metrics Used:

Support: Frequency of an itemset in all transactions.

Confidence: Likelihood that an item Y is bought when item X is bought.

Lift: Strength of association; values > 1 indicate a positive relationship.

 Libraries Used

pandas – for data manipulation and display

mlxtend – for TransactionEncoder, apriori, and association_rules functions

 Installation

To run this notebook, install the required libraries:

pip install mlxtend pandas

 Dataset Description

A small, hard-coded dataset simulates shopping baskets, where each list represents items purchased in one transaction:

dataset = [
    ['Milk', 'Bread', 'Eggs'],
    ['Bread', 'Diapers', 'Beer', 'Eggs'],
    ['Milk', 'Diapers', 'Bread', 'Cola'],
    ['Bread', 'Eggs'],
    ['Milk', 'Bread', 'Diapers', 'Eggs'],
    ['Cola', 'Diapers', 'Beer'],
    ['Milk', 'Bread', 'Cola'],
    ['Bread', 'Diapers', 'Eggs'],
]

 Methodology

Convert the dataset to a one-hot encoded DataFrame using TransactionEncoder.

Apply the Apriori algorithm with a minimum support threshold of 0.6.

Generate association rules with a minimum confidence threshold of 0.7.

Display the resulting frequent itemsets and rules.

 Sample Output

Frequent Itemsets:

   support            itemsets
0    0.625             (Bread)
1    0.625              (Eggs)
2    0.625  (Bread, Eggs)


Association Rules:

  antecedents consequents  support  confidence      lift
0     (Bread)      (Eggs)    0.625    0.714286  1.142857
1      (Eggs)     (Bread)    0.625    1.000000  1.142857

 Interpretation

When customers buy Bread, they also buy Eggs with a 71% confidence.

When Eggs are purchased, Bread is always bought (100% confidence).

The lift value (1.14) indicates a slightly positive correlation between the two items.

 File

Association.ipynb – Jupyter notebook containing the full code and output.

 Learning Outcome

This project helps you understand the basics of association rule mining and how to implement it in Python using mlxtend.
