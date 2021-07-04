# Unit 11 - Risky Business

------------------

## Resampling


### **Objective:**

Use the imbalanced learn library to resample the LendingClub data and build and evaluate logistic regression classifiers using the resampled data.

### **Data Preparation**

The LendingClub CSV data was read and split into training and testing sets.  The data was then scaled using the StandardScaler.

### **Simple Logistic Regression**

The regression model was fitted to the training set and the balanced accuracy score was calculated: 0.9543211898288821

The confusion matrix was then displayed:

![](images/simple_regression_confusion_matrix.png)

The imbalanced classification report was printed:

![](images/simple_classification_report.png)

### **Oversampling**

The data was oversampled using the Naive Random Oversampler and SMOTE algorithms.

The Naive Random Oversampling had a balanced accuracy score of: 0.9543211898288821

The confusion matrix:

![](images/naive-random-confusion.png)

The imbalanced classification report:

![](images/naive-random-imbalanced.png)

The SMOTE Oversampling had a balanced accuracy score of: 0.9948279972279972

The confusion matrix:

![](images/smote-confusion.png)

The imbalanced classification report:

![](images/smote-imbalanced.png)

### **Undersampling**

The data was then undersampled using the Cluster Centroids algorithm.

The balanced accuracy score was: 0.9828813049736127

The confusion matrix:

![](images/cluster-confusion.png)

The imbalanced classification report:

![](images/cluster-imbalanced.png)


### **Combincation (Over and Under) Sampling**

The data was over- and under- sampled using the SMOTEENN algorithm.

The balanced accuracy score: 0.994748035609574

The confusion matrix:

![](images/smoteenn-confusion.png)

The imbalanced classification report:

![](images/smoteenn-imbalanced.png)


### **Conclusion**

The SMOTE Oversampling model had the best balanced accuracy score of 0.9948279972279972.  All of the models had the same recall score of 0.99.  The Naive Random Oversampling, SMOTE Oversampling, and SMOTEENN Combo Sampling all had a geometric mean score of 0.99.


## Ensemble Learning

### **Objective**
Train and compare the Balanced Random Forest and Easy Ensemble classifiers to predict loan risk and evaluate each model. 

### **Data Preparation**
2019 Q1 Loan Stats CSV data was read and split into training and testing sets.  The data was then scaled using StandardScaler

### **Balanced Random Forest Classifier**
balanced accuracy score: 0.8162470639899118

confusion matrix: 

![](images/brf-confusion.png)

imbalanced classification report: 

![](images/brf-imbalanced.png)

List of top 10 features in descending order of feature importance: 

![](images/brf-feature-importance.png)


### **Easy Ensemble Classifier**
balanced accuracy score: 0.9263912558266958

confusion matrix: 

![](images/easy-confusion.png)


imbalanced classification report: 

![](images/easy-imbalanced.png)

### **Conclusion**

The Easy Ensemble Classifier model had the best balanced accuracy score of 0.9263912558266958.    The Easy Ensemble Classifier had the best recall score of 0.94.      The geometric score did not appear in the classification report.    The top three features for the Balanced Random Forest Classifier weren total_rec_prncp, total_rec_int, and total_pymnt_inv.  Their values were 0.07440136919465735, 0.061437291161306265, and 0.06130032888752441, respectively.
