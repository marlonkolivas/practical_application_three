## Practical Application III: Comparing Classifiers

**Overview:** In this practical application, your goal is to compare the performance of the classifiers we encountered in this section, namely K Nearest Neighbor, Logistic Regression, Decision Trees, and Support Vector Machines. We will utilize a dataset related to marketing bank products over the telephone.

#### Summary
---
This analysis evaluates the effectiveness of the bank’s telemarketing campaign using classification modeling. The goal is to determine which clients are most likely to subscribe to a term deposit, enabling the organization to optimize targeting efforts and campaign resources.

Four classification models were trained and compared based on:
- Training time
- Training accuracy
- Testing accuracy

The model with the best combination of high test accuracy and reasonable training time is recommended for future use in campaign targeting.

#### Objective of the study
---
The bank conducts direct telemarketing campaigns to promote term deposits. However, these campaigns require extensive time and labour, and conversion rates remain low due to the untargeted nature of the outreach.

Objective:
1. Train and evaluate four classification models to predict whether a client will subscribe to a term deposit.
2.  Compare model performance using training time, training accuracy, and testing accuracy.
3.	Identify key insights that can help improve future campaign efficiency and conversion rates.

#### Dataset
---
Dataset: Bank Marketing Campaign Dataset <br>
Source: UCI Machine Learning Repository <br>
Link: [Bank Marketing - UCI Machine Learning Repository ](https://archive.ics.uci.edu/ml/datasets/bank+marketing)

#### Data Preparation Summary
---
Preparation steps completed prior to modeling:
- Converted target column (y) to binary (1 = subscribed, 0 = not subscribed).
- One-hot encoded categorical variables.
- Scaled numerical features when required (e.g., for KNN or SVM).
- Split into training and testing datasets (e.g., 80% train / 20% test).

These steps ensure consistent formatting and fairness across trained models.

#### Classification Modeling
---
**Models Trained**<br>
The following four classifiers were trained:
1. Logistic Regression
2. K-Nearest Neighbors (KNN)
3. Decision Tree Classifier
4. Support Vector Machine (SVM)

Each model was trained using identical train-test splits to ensure fair comparison.

**Performance Evaluation**<br>
Performance was assessed using:
- Training Time (seconds) — efficiency
- Training Accuracy — how well the model fits known data
- Testing Accuracy — generalization performance (ability to predict new clients)

#### Insights
---
1. **SVM (RBF Kernel):**
- Demonstrated the longest training time, significantly higher than the other models.
- Despite the heavy computational cost, it did not achieve the highest test accuracy, indicating that the added complexity and non-linear kernel did not provide sufficient predictive benefit for this dataset.
- This inefficiency is particularly relevant when scaling to larger datasets or when retraining models frequently.
  
2. **K-Nearest Neighbors (KNN) and Decision Tree:**
- Had moderate training times and performed adequately, but did not surpass Logistic Regression in test accuracy.

3. **Logistic Regression:**
- Combined fast training with high test accuracy, making it the most reliable model in terms of balancing computational efficiency and predictive performance.
- Its simplicity ensures easy deployment and interpretability for business stakeholders, allowing decisions to be communicated clearly and acted upon confidently.

#### Recommendation
---
Considering both effiency and performance, logistic regression is the recommended model for this bank campaign dataset
