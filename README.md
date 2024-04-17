# credit-risk-classification

Utilizing machine learning techniques, an analysis was conducted on a dataset encompassing historical lending activities from a peer-to-peer lending services firm with the aim of constructing a model capable of assessing the creditworthiness of borrowers.

Overview of the Analysis:
The analysis considered various factors including:
-Loan size
-Interest rate
-Borrower's income
-Debt-to-income ratio
-Number of borrower's accounts
-Derogatory marks against the borrower
-Total debt

The dataset, comprising 77,536 data points, underwent division into training and testing sets. The training set facilitated the construction of an initial logistic regression model (Logistic Regression Model 1) using the LogisticRegression module from scikit-learn. Subsequently, Logistic Regression Model 1 was applied to the testing dataset to ascertain whether loans to borrowers would be categorized as low- or high-risk.

The initial model was developed from a dataset consisting of 75,036 low-risk loan data points and 2,500 high-risk data points. To equalize the number of data points accessible for logistic regression modeling, the training set data underwent resampling using the RandomOverSampler module from imbalanced-learn. This resampling process resulted in the generation of 56,277 data points for both low-risk (0) and high-risk (1) loans, preserving the original dataset's proportions.
The resampled data was employed to construct a new logistic regression model (Logistic Regression Model 2), aimed at determining the risk level (low or high) of loans to borrowers within the testing set. The ensuing results are outlined below:

Results:
Logistic Regression Model 1:
-Precision: 93% (average precision)
-Accuracy: 94%
-Recall: 95% (average recall)

Logistic Regression Model 2:
-Precision: 93% (average precision)
-Accuracy: 100%
-Recall: 100%

Summary:
Logistic Regression Model 2 exhibits reduced likelihood of predicting false negative results. However, when comparing the confusion matrices for each model, it becomes apparent that Logistic Regression Model 2 predicted slightly more false positives (classifying loans as low-risk when they were actually high-risk).

Neither model achieves precision scores above 90% if the objective is to determine the likelihood of high-risk loans. Nevertheless, Logistic Regression Model 2 displays fewer false predictions overall on the testing data, thereby positioning it as the preferred model due to its high accuracy and recall rates.