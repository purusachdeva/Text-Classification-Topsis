# TOPSIS Analysis with Python

## Description

### Input Data

The Python script reads a CSV file named "model_metrics.csv" containing a decision matrix. The columns of this matrix represent different criteria, such as Accuracy, Training Time, and Model Size, for various models.

#### Models Used in the Analysis

The decision matrix includes the following models:

- BERT
- GPT-3
- XLNet
- RoBERTa
- DistilBERT
- ALBERT
- ERNIE
- ULMFiT
- FastText
- CLIP

### TOPSIS Analysis

The TOPSIS analysis is performed using the `topsis_analysis` function. The function takes the input file path, weights, and impacts as parameters.

- **Weights:** The weights are specified as a comma-separated string (e.g., "0.4,0.3,0.3").
- **Impacts:** The impacts are specified as a string of '+' and '-' symbols corresponding to the desired impact for each criterion (e.g., "+,-,-").

The `topsis` function normalizes the decision matrix, calculates the weighted normalized decision matrix, identifies positive and negative ideal solutions, and computes TOPSIS scores and ranks.

### Visualization

The Python script generates and saves a bar plot illustrating TOPSIS scores for each alternative. The plot is shown below:

![TOPSIS Scores Bar Plot](topsis_scores_bar_plot.png)

Additionally, a table with TOPSIS results, including scores and ranks, is saved as a CSV file.

## Usage

To execute the TOPSIS analysis, run the Python script by providing the appropriate input file, weights, and impacts.

```python
input_file = "model_metrics.csv"
weights_str = "0.4,0.3,0.3"
impacts_str = "+,-,-"
output_file = "outputs.csv"
topsis_analysis(input_file, weights_str, impacts_str, output_file)
