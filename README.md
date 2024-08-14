# Loan Default Data Analysis
See `.ipynb.` for a detailed walk-through.

## Overview
This project analyzes loan default data to identify key factors that influence whether a loan is fully paid or not. The analysis includes data exploration, visualization, and statistical testing, such as correlation analysis, to uncover relationships between various loan features and their impact on default rates.

## Project Structure
- **LoanDefaultDataAnalysis.ipynb**: The Jupyter Notebook containing the full analysis of the loan default data. This notebook includes data cleaning, exploration, visualization, and statistical analysis.
- **Data_Loan.csv**: CSV spreadsheet consisting of 100 entries for loans along with features and outcomes.

## Key Features
- **Data Exploration**: Initial exploration of the dataset to understand its structure and contents.
- **Correlation Analysis**: Identifying significant correlations between different features in the dataset for both paid and unpaid loans.
- **Visualization**: Various plots such as scatter plots, regression lines, and heatmaps to visually represent the relationships between variables.
- **Statistical Testing**: Conducted Chi-Squared tests and other statistical analyses to identify significant associations between categorical variables and loan status.

## Installation
To run this analysis, you will need to have Python and Jupyter Notebook installed. The key libraries used in this project include:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scipy`

You can install the necessary packages using pip:

```bash
pip install pandas numpy matplotlib seaborn scipy
```

## Usage
To reproduce the analysis:

1. Clone this repository:
    ```bash
    git clone https://github.com/yourusername/LoanDefaultDataAnalysis.git
    ```
2. Navigate to the project directory:
    ```bash
    cd LoanDefaultDataAnalysis
    ```
3. Open the Jupyter Notebook:
    ```bash
    jupyter notebook LoanDefaultDataAnalysis.ipynb
    ```
4. Run the cells in the notebook to perform the analysis.

## Key Insights
### Paid Borrowers:
- **DTI and interest rate**: Positive correlation of +0.41.
- **FICO score and interest rate**: Strong negative correlation of -0.85.
- **Revolving utilisation rate and interest rate**: Positive correlation of +0.71.

### Unpaid Borrowers:
- **DTI and interest rate**: Negative correlation of -0.36.
- **Revolving balance and log annual income**: Positive correlation of +0.79.
- **Revolving utilisation rate and DTI**: Negative correlation of -0.70.

These insights indicate that certain factors, such as FICO score and interest rate, have a significant impact on whether a loan is paid or not.

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

### Customization:
- **Overview**: Customize the overview to reflect any specific goals or outcomes of your analysis.
- **Key Features**: Modify based on what the notebook specifically accomplishes.
- **Installation**: Ensure the correct libraries and versions are listed.
- **Key Insights**: Adjust based on the actual findings from your analysis.

If you want more specific details to be included or have any additional sections you'd like to add, feel free to ask!