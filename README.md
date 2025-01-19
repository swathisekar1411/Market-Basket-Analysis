# Market Basket Analysis

This repository contains a Python implementation of Market Basket Analysis using the Apriori algorithm. The analysis aims to uncover associations and patterns in transactional data. The provided code utilizes the `mlxtend` library for frequent pattern mining and association rule generation.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Requirements](#requirements)
- [Usage](#usage)
- [File Descriptions](#file-descriptions)
- [Results](#results)
- [License](#license)

## Overview

Market Basket Analysis is a data mining technique used to identify relationships between items purchased together. In this project, the analysis is performed on transactional data, with insights extracted at both product and category levels.

## Features

- Data preprocessing and cleaning, including handling missing values and standardizing data formats.
- Categorization of products into broader categories for enhanced analysis.
- Encoding transactional data using hot encoding for compatibility with Apriori.
- Frequent itemset mining and association rule generation using the Apriori algorithm.
- Support and lift metrics for evaluating association rules.

## Requirements

This code is implemented in Python and requires the following libraries:

- `numpy`
- `pandas`
- `mlxtend`
- `openpyxl` (for handling Excel files)

To install the required libraries, run:

```bash
pip install numpy pandas mlxtend openpyxl
```

## Usage

1. **Prepare the Data**
   - The input data should be an Excel file named `market_analysis.xlsx` with a sheet named `Chat Orders`.
   - Ensure the data contains columns such as `Order ID`, `Cart`, and `Quantity`.

2. **Run the Code**
   - Execute the script to clean and preprocess the data.
   - The transactional data will be encoded and saved to `market_analysis.xlsx`.

3. **Generate Association Rules**
   - The Apriori algorithm is applied at both product and category levels.
   - Frequent itemsets and association rules will be generated and displayed in the output.

## File Descriptions

- `Market Basket Analysis.ipynb`: The main notebook containing the implementation of the analysis.
- `market_analysis.xlsx`: The input dataset for analysis. The file will also store preprocessed data and results.

## Results

The output includes:

- Frequent itemsets with their support values.
- Association rules with metrics such as confidence and lift.

Example output for association rules:

| Antecedents         | Consequents        | Support | Confidence | Lift  |
|---------------------|--------------------|---------|------------|-------|
| {Product A}         | {Product B}       | 0.07    | 0.85       | 3.00  |
| {Category X, Y}     | {Category Z}      | 0.10    | 0.75       | 2.50  |

