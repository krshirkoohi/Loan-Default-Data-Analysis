# Loan-Default-Data-Analysis

## Information

### Data dictionary
* `credit_policy`: Whether the applicant meets basic credit criteria
* `purpose`: The stated purpose of the loan
* `int_rate`: The interest rate assigned to the loan
* `installment`: Monthly payment amount
* `log_annual_inc`: Natural log of the applicant's annual income
* `dti`: Debt-to-income ratio
* `fico`: FICO credit score
* `days_with_cr_line`: Length of credit history
* `revol_bal`: Revolving balance
* `revol_util`: Revolving utilisation rate
* `inq_last_6mths`: Number of credit inquiries in the last 6 months
* `delinq_2yrs`: Number of delinquencies in the past 2 years
* `pub_rec`: Number of derogatory public records
* `not_fully_paid`: Target variable (1 if the loan was not fully paid, 0 if it was)

## Report

### Abstract
A loan default occurs when a borrower fails to make necessary payments on their debt. We will investigate quantitative factors which contribute to a borrower being unable to pay back a loan, using exploratory data analysis. We’ll use these findings to determine whether to approve future loan applications.

### Aims and objectives
The task is to perform an EDA on the data set to uncover patterns and trends. We’ll answer the following questions
- What makes a good borrower versus a bad one?
- What variables can we control to reduce the likelihood of defaults?
- What are the limitations of the data?

### Methodology
A data set of 100 loans in CSV format was loaded into Python using the Pandas module. The data was cleaned, and transformed to remove redundant columns, and remaining columns were sorted into categorical and numerical sub sets `df_cat` and `df_num`. 

Within these sub sets, the fundamental statistics were obtained, and univariate and bivariate analysis was conducted to investigate `not_fully_paid`, the status of a default on a loan.
