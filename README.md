# Facebook vs. AdWords Marketing Campaign Analysis

This project demonstrating a comparative analysis of two marketing campaigns using Python. This repository contains the Jupyter Notebook and data required to reproduce the analysis, which includes A/B testing, hypothesis testing, and a simple linear regression model.

## Overview

This project analyzes a synthetic dataset of two year-long advertising campaigns, one on Facebook and one on AdWords, to determine which platform is more effective. The analysis identifies the better-performing platform based on conversions and clicks and builds a predictive model for the winning campaign.

## Features

* **Exploratory Data Analysis (EDA)**: Visualizations of click and conversion distributions.
* **A/B Hypothesis Testing**: A two-sample independent t-test to determine if there is a statistically significant difference in conversions between the two platforms.
* **Correlation Analysis**: Measures the relationship between ad clicks and conversions.
* **Predictive Modeling**: A simple linear regression model to forecast Facebook ad conversions based on clicks.

## Project Structure

<img width="517" height="177" alt="image" src="https://github.com/user-attachments/assets/b30b3fbc-cc1c-45c7-b5df-bdfd7333e4a6" />

## Installation

To run this analysis on your local machine, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone <repository-url>
    cd <repository-directory>
    ```

2.  **Set up a virtual environment (recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install the required libraries:**
    A `requirements.txt` file is not included, but you can install the necessary packages using pip:
    ```bash
    pip install pandas matplotlib seaborn scipy numpy scikit-learn statsmodels jupyter
    ```

## Usage

1.  **Start Jupyter Notebook:**
    Once the libraries are installed, launch the Jupyter Notebook server from your terminal:
    ```bash
    jupyter notebook
    ```

2.  **Run the Analysis:**
    In the Jupyter interface that opens in your browser, click on `AB Testing (Marketing Campaigns).ipynb` to open the notebook. You can then run the cells sequentially to execute the analysis.

## Analysis and Findings Summary

The detailed analysis is in the notebook. Here is a high-level summary of the findings:

### Key Result Visualization

The bar chart below (generated in the notebook) shows the frequency of days falling into different conversion categories. It clearly illustrates that the Facebook campaign had significantly more high-conversion days (10-15 and >15 conversions) than the AdWords campaign, which had none in these upper brackets.

*(This chart is generated in the "Comparing Campaigns performance" section of the notebook.)*

### Summary of Findings

1.  **Facebook Outperforms AdWords**: The analysis shows that the Facebook campaign resulted in a statistically significant higher mean number of conversions (11.74) compared to AdWords (5.98).
2.  **Stronger Click-to-Conversion Link on Facebook**: There is a strong positive correlation (0.87) between clicks and conversions for Facebook, whereas AdWords shows a moderate correlation (0.45).
3.  **Predictive Model**: A linear regression model predicted Facebook conversions from clicks with an R-squared score of 76.35%. For example, the model predicts that 50 clicks would result in approximately 13 conversions.

## Methodology Notes

* **Hypothesis Test**: An independent two-sample t-test was used to compare the means of the conversion data from the two platforms. The p-value was significantly below 0.05, leading to the rejection of the null hypothesis (that there is no difference).
* **Regression**: A simple linear regression (`sklearn.linear_model.LinearRegression`) was fit with `Facebook Ad Clicks` as the independent variable and `Facebook Ad Conversions` as the dependent variable.

## Limitations

* **Synthetic Data**: The dataset used is synthetic and contains exactly 365 entries for 2019. It is intended for demonstrating analytical techniques rather than drawing real-world business conclusions.
* **Simplistic Model**: The regression model is a simple linear model and does not account for other potential factors like seasonality, ad spend, or creative variations.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
