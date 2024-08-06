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

#### Notes on data
- The log of the annual income of a borrower is used to factor out [diminishing returns](https://typeset.io/questions/why-use-log-of-household-income-when-estimating-the-1n2q29zfle#) on the impact of wellbeing as a household’s wealth increases.
- We assume currency is in GBP.
Sample size
Of 100 loan outcomes surveyed, 10 were unpaid. The data set is small, having an even smaller subset for the target data points. An obvious suggestion would be to use more data points, particularly since univariate analysis on such as small sample size can yield unreliable results. A larger figure such as 1000 loans would be a better number, using the framework developed here to analyse the new amount.

Since the proportion of failed payments is much smaller than that of the paid loans, we could look at the problem from a different perspective, analysing what contributes to a loan being paid successfully. We could then profile the failed payment loans onto this analysis, and comment on the cases where these cases differ.

### Results and discussion

#### Numerical statistics
Total accounts analysed N=100.

Paid (n=90):
| Measure                    | Average | Min    | Max      |
|----------------------------|---------|--------|----------|
| Interest rate              | 0.099   | 0.071  | 0.160    |
| Installment amount         | £223.50 | £39.60 | £829.10  |
| Log of annual income       | 11.1    | 8.99   | 12.4     |
| Debt-to-income ratio       | 8.76    | 0      | 22.1     |
| Days with credit line      | 4634    | 1127   | 14009    |
| Revolving balance          | £17,189 | £0     | £128,000 |
| Revolving utilisation rate | 33.9    | 0      | 93.4     |
| FICO credit score          | 729     | 627    | 812      |

Unpaid (n=10):
| Measure                    | Average | Min    | Max     |
|----------------------------|---------|--------|---------|
| Interest rate              | 0.120   | 0.096  | 0.150   |
| Installment amount         | £267.97 | £32.55 | £678.08 |
| Log of annual income       | 10.6    | 9.62   | 12.27   |
| Debt-to-income ratio       | 11.5    | 2.86   | 20.0    |
| Days with credit line      | 3912    | 1110   | 6240    |
| Revolving balance          | £15,398 | £269   | £56,411 |
| Revolving utilisation rate | 50.3    | 3.8    | 76.8    |
| FICO credit score          | 701     | 667    | 772     |

#### Data distribution 

![](CleanShot%202024-08-03%20at%208%E2%80%AF.04.00@2x.png)
>Holding a public derogatory record, and credit enquiries within the past 6 months appear to have some influence on the borrower not being able to pay a loan. This is confirmed by the inverse being true by looking at the cases where the loan is paid.