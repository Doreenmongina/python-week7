# Mobile Phone Dataset Analysis

## Objective

The primary objectives of this assignment were to:

* Load and analyze a mobile phone dataset using the pandas library in Python.
* Perform basic data exploration and cleaning to prepare the dataset for analysis.
* Conduct basic data analysis, including descriptive statistics and group comparisons.
* Create informative visualizations using the matplotlib and seaborn libraries to identify patterns and trends in the data.
* Document the entire process, including code, observations, and findings.

## Submission Requirements Checklist

This submission includes:

* [x] A Jupyter notebook (.ipynb file) or Python script (.py file) containing all code.
* [x] Data loading and exploration steps clearly documented.
* [x] Basic data analysis results presented and explained.
* [x] At least four different types of visualizations with proper customization.
* [x] A section on findings and observations derived from the analysis.

## Task 1: Load and Explore the Dataset

### Loading the Dataset

The mobile phone dataset, stored in 'Mobiles_Dataset_2025.csv', was loaded into a pandas DataFrame using the `pd.read_csv()` function. The `encoding='latin-1'` parameter was used to handle potential character encoding issues within the file. Error handling using a `try-except` block was implemented to gracefully manage scenarios where the file might not be found or if any other error occurs during the loading process.

```python
import pandas as pd

try:
    df = pd.read_csv('Mobiles_Dataset_2025.csv', encoding='latin-1')
    print("Successfully loaded the dataset!")
except FileNotFoundError:
    print("Error: The file 'Mobiles_Dataset_2025.csv' was not found. Please make sure the file is in the correct directory or its named correctly.")
    exit()
except Exception as e:
    print(f"An error occurred while loading the dataset: {e}")
    exit()
