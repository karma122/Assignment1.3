By: Jeshal Mohapatra, Krish Tiwari, Varsha Iynger, Hugo Vides
QUESTIONS TO ANSWER

Q1)
Loading unnecessary libraries consumes memory, which can slow down the execution of the notebook.
Fewer libraries mean faster execution times for the notebook.
Minimizing the number of external dependencies reduces potential security vulnerabilities in the code.


Q2) To check for missing data, we used the “.isnull().sum()” method. This method will return the count of missing values for each column. If the count is zero for all columns, it means there are no missing values in the dataset. Otherwise, the columns with non-zero counts have missing data.

This output indicates that there are no missing values in the dataset as it is all 0.

Q3)

1. Numeric Data:
   - Using the mean value maintains the central tendency of the data, ensuring that the overall statistical properties of the dataset remain consistent.
   - The mean is easy to calculate and use for imputation.
   - For normally distributed data, the mean is a good representative value.

2. Non-Numeric Data:
   - Non-numeric data often consists of categories or labels. The mode represents the most frequent category, making it a logical choice for imputation.
   - Imputing with the mode maintains the distribution of categories in the dataset.
   - Like the mean, the mode is straightforward to compute and apply.

Q4)
Industry variables: These variables are mostly binary (0 or 1), indicating whether a client belongs to a particular industry. Mostly 0.
Ethnicity variables: These variables are also mostly binary (0 or 1), representing different ethnicities. Mostly 0 as well.
Years employed: Right-skewed distribution with most clients having fewer years of employment.
Prior default: Also binary which shows a large proportion of clients with 0 (no prior default) compared to 1, which was prior default.
Employed: Binary variable where a large proportion of clients are employed (1) compared to those not employed (0).
CreditScore: Right-skewed, with most clients having lower credit scores. 
DriversLicense: Another binary variable indicates whether clients have a driver’s license. The histogram shows a large number of clients with a driver’s license (1) compared to those without (0).
Citizen Variables: These binary variables represent different citizenship statuses. Most clients fall into the Citizen_0 category.
ZipCode: The histogram shows a right-skewed distribution with most clients having lower ZipCode values.
Income: The histogram is heavily right-skewed with most clients having lower incomes.
Approved: This binary variable indicates whether the loan was approved. The histogram shows a somewhat balanced distribution, with a slightly higher number of 0s (not approved) compared to 1s (approved).

Q5)
Strong Positive Correlation
There are several variables with high positive correlations (values close to 1). For example, the "Industry" columns have a strong correlation with each other because these are binary variables that are one hot encoded, where only one of them can be 1 and the rest must be 0 for any given row.
"Ethnicity" columns show a similar pattern of high positive correlation due to one-hot encoding.
Strong Negative Correlations
There are strong negative correlations (values close to -1) between the "Industry" columns and the "Ethnicity" columns. This is because these columns are mutually exclusive categories.
Relationships with Target Variable (Approved)
In the heatmap, we can see if there are any variables that have a significant correlation with the "Approved" variable since it’s the target variable. 
From the heatmap, it appears "Income" might have a positive correlation with "Approved," which suggests that higher income means higher approval rates.
The variable "PriorDefault" seems to have a strong negative correlation with "Approved,".
No or Weak Correlation
Some variables may have very weak or no correlation with each other (values close to 0). These variables are likely independent of each other.
For example, "YearsEmployed" and "CreditScore" do not show strong correlation with other features.

Q6) 
Splitting the data into training and testing sets allows us to evaluate the performance of the model on unseen data.
By testing the model on a separate test set, we can detect overfitting. A model that performs well on the training data but poorly on the test data is likely overfitting.
Splitting the data allows us to compare the performance of different models or algorithms on the same test set. This helps in selecting the best model for the task at hand.
The performance of a model on the test set provides an estimate of how the model will perform in real-world scenarios, where it’s meant to be used. This is crucial for applications where model predictions have significant consequences, such as in finance and tech. 




