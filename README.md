Customer Churn Prediction 

Introduction
This project focuses on predicting customer churn using various machine learning models. The goal is to identify factors contributing to customer churn and to enhance customer retention strategies by analyzing demographic, service, and account-related information.

Dataset Description
The dataset contains demographic, service, and account information for customers, with the following features:
•	Demographic Information: Gender, Age Range, Partner, Dependents
•	Services Information: Phone services, Multiple lines, Internet services, Online Security, Online Backup, Device Protection, Tech Support, Streaming TV/Movies
•	Account Information: Tenure, Contract type (month-to-month, one-year, two-year), Payment Method, Paperless Billing, Monthly Charges, Total Charges
•	Churn (Target Variable): Indicates whether a customer has discontinued service.

Data Cleaning and Preprocessing
•	Consistency Adjustments: Replaced 'No Internet service' with 'No' in relevant columns.
•	Simplified Payment Methods: Removed descriptors like '(automatic)' from the PaymentMethod field.
•	Feature Streamlining: Removed unnecessary columns like Customer ID and Tenure.
•	Numerical Conversion: Converted SeniorCitizen field from binary to categorical ('Yes', 'No').
•	Encoding: Applied one-hot encoding to categorical variables.
•	Handling Missing Values: Removed 11 entries with missing TotalCharges and Tenure values of 0.

Exploratory Data Analysis (EDA)
•	Key Insights:
o	Customers with longer-term contracts are less likely to churn.
o	Customers without Online Security are more likely to churn.
o	Churn rates are higher for customers with Fiber Optic services.
o	Customers paying with electronic checks tend to churn more frequently.
•	Correlation Results:
o	Tenure: Negative correlation with churn, indicating longer-tenured customers are less likely to churn.
o	Monthly Charges: Positive correlation with churn, meaning higher charges may increase churn likelihood.
o	Total Charges: Negative correlation, implying that higher total charges (often due to longer tenure) reduce churn likelihood.

Models Used and Performance
1.	Logistic Regression:
o	Accuracy: 79%
o	Stronger in predicting "No Churn" but weaker in predicting "Churn."
2.	Decision Tree:
o	Accuracy: 72%
o	Similar issues with churn prediction accuracy compared to Logistic Regression.
3.	Gradient Boosting Classifier:
o	Accuracy: 80.73%
o	Best performer with high precision for "No Churn" (85%) and moderate precision for "Churn" (66%).
4.	Random Forest:
o	Accuracy: 80%
o	Good recall for "No Churn" (91%), but struggles with "Churn" prediction (49% recall).

Model Comparison
•	Overall Accuracy: Gradient Boosting is the top performer with 80.73% accuracy.
•	Performance on Churn (Class 1): Gradient Boosting offers the best precision for churn prediction (66%).
•	No Churn (Class 0): Random Forest and Gradient Boosting show strong performance, with over 90% recall.

Conclusion
Gradient Boosting stands out as the most effective model, particularly in churn prediction where accurate identification of both classes is crucial. Random Forest and Logistic Regression also perform well, especially in predicting customers unlikely to churn.

Future Work
•	Time Series Analysis: Incorporating temporal patterns in customer behavior for enhanced accuracy.
•	Ensemble Methods: Exploring advanced techniques such as stacking to improve prediction accuracy.
•	Deep Learning: Investigating neural networks for large datasets to capture complex non-linear relationships.
•	AutoML: Utilizing automated machine learning tools to fine-tune models and hyperparameters systematically.



How to Run the Project
1.	Clone the repository.
2.	Install required dependencies using pip install -r requirements.txt.
3.	Run the Jupyter Notebook Customer Churn Pred.ipynb to reproduce the analysis and models.

