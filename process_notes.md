General Notes:

- Had an issue with bringing in the file. I was a .xls file and wouldn't load so I turned it into a .csv file. I opened up the .xls file, saved it as a csv. It worked after that. 

- Need to create a pipleline. The models I want to use are:
(Logistic Regression, LDA, QDA, and KNN)

- The dataset is not split into train and test from the beginning so maybe that can be part of the pipeline. Importing pathlib and train_test_split to help create paths for the new files and split into train/test files.

- having issues getting sklearn to work on VSCode. 

Cleaning Notes:

- The dataset has no cleaning needed from first glance. All rows are there, no nulls. Also there all int64 right now. I believe the only thing that needs to be done is dummying. Some of the rows that need to be dummy'd are sex, education, marriage.
- Where is PAY_1?
- There is a value in the X6-X11 columns of 0. If -1 = pay duly and 1 is payment delay for one month, is 0 paid on time or is that actually a null? 


Questions/Hypothesis:

Data Dictionary:

X1: Amount of the given credit (NT dollar): it includes both the individual consumer credit and his/her family (supplementary) credit.
X2: Gender (1 = male; 2 = female).
X3: Education (1 = graduate school; 2 = university; 3 = high school; 4 = others).
X4: Marital status (1 = married; 2 = single; 3 = others).
X5: Age (year).
X6 - X11: History of past payment. We tracked the past monthly payment records (from April to September, 2005) as follows: X6 = the repayment status in September, 2005; X7 = the repayment status in August, 2005; . . .;X11 = the repayment status in April, 2005. The measurement scale for the repayment status is: -1 = pay duly; 1 = payment delay for one month; 2 = payment delay for two months; . . .; 8 = payment delay for eight months; 9 = payment delay for nine months and above.
X12-X17: Amount of bill statement (NT dollar). X12 = amount of bill statement in September, 2005; X13 = amount of bill statement in August, 2005; . . .; X17 = amount of bill statement in April, 2005.
X18-X23: Amount of previous payment (NT dollar). X18 = amount paid in September, 2005; X19 = amount paid in August, 2005; . . .;X23 = amount paid in April, 2005.

Concepts to understand:

Logistic Regression
LDA
QDA
Confusion Matrix
Maximum Likelihood
Decision Boundary


Resources:

Creating a Pipeline: https://medium.com/vickdata/a-simple-guide-to-scikit-learn-pipelines-4ac0d974bdcf

Automating workflows with pipelines: https://machinelearningmastery.com/automate-machine-learning-workflows-pipelines-python-scikit-learn/