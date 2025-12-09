# Trial
base code submission
RMSE=457.3909203668297

# Submission 1 
Model with all columns except the missing value columns
RMSE=261.87413168602234

# Submission 2
Impute values in variables with missing values.
education_level: Mode Imputation
online_shopping_freq: Right skewed so median imputation
utility_payment_count: Right skeweed hence median imputation
RMSE=257.39143476396436

# Submission 3
Best Subset selection with the submission 2 imputations and using the Multiple Linear regression model.
RMSE=257.39685289133104      Less than submission 2

# Submission 4
In this submission I build on the submission 3 backward selection method. I used all variables that were used for submission 3. Then for numeric variables I perform EDA and then look for anytransformations.
Majority of the variables were right skewed hence I applied log transformation to the right skewed variables.
Basic EDA for categorical variables was done but we use them as they are from the submission 3.
RMSE=277.70931827231027

# Submission 5
Now I will try the MICE algorithm to fill in the missing values and then test it based on the best working submission 3. Train Test split was used and data was trained using the train dataset.
Resulted in Lower test rmse score but not performed well in the actual scoring dataset.

# Submission 6
Lets use the same method in submission 5 and train on full train dataset.
It was able to reduce the score to the lowest of first 5.

# Submission 7
Lets try out Median use instead of Mean in the Imputer of 6 th submission.
The mean imputation worked better.

# Submission 8
STandardize variables before regression. Performed well but didn't beat the mean imputation with MICE in submission 6.

# Submission 9
Tried Ridge, worked well. Transformed Y then tried ridge worked poorly.

# Submissions 11
Polynomial degree 3 with elasticnet. SSubmit this

# Submission 15
Target encoding polynomial elastic net submit this.