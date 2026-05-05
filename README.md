# ML-Project
📄 MINI PROJECT REPORT
Student Performance & Placement Prediction using Machine Learning
1. Introduction

Machine Learning (ML) is a branch of artificial intelligence that enables systems to learn from data and make predictions or decisions without being explicitly programmed. It is widely used in areas such as education, healthcare, finance, and business analytics.

In the education domain, predicting student performance and placement outcomes can help institutions identify weak students, improve teaching strategies, and increase placement success rates.

This project uses various Machine Learning algorithms to analyze student data and predict:

Final Exam Score (Regression Problem)
Placement Status (Classification Problem)
2. Objective

The main objectives of this project are:

To predict student academic performance using regression algorithms
To classify whether a student will be placed or not
To compare the performance of different Machine Learning algorithms
To identify patterns affecting student success
3. Dataset Description

A custom dataset named student_data.csv is used for this project.

Attributes:
Feature	Description
Age	Age of student
Gender	Male/Female
Study_Hours	Daily study time
Attendance	Attendance percentage
Internal_Marks	Internal exam marks
Assignment_Score	Assignment performance
Internet_Usage	Low/Medium/High
Extra_Activities	Participation in activities
Sleep_Hours	Average sleep duration
Final_Exam_Score	Final exam marks
Placed	Placement status (Yes/No)
4. Algorithms Used
4.1 Decision Tree
Used for classification
Creates a tree-like model of decisions
Easy to interpret
4.2 Simple Linear Regression
Predicts final score using one variable (Study Hours)
Establishes a linear relationship
4.3 Multiple Linear Regression
Uses multiple inputs (Attendance, Marks, etc.)
Provides better prediction accuracy
4.4 Logistic Regression
Used for binary classification (Placed / Not Placed)
Uses sigmoid function
4.5 Support Vector Machine (SVM)
Finds optimal boundary between classes
Effective for complex datasets
4.6 K-Nearest Neighbors (KNN)
Classifies based on nearest data points
Simple and effective
4.7 Naïve Bayes
Based on probability theory
Assumes feature independence
4.8 Association Rule Mining (Apriori)
Finds relationships between features
Example: High study hours → High scores
5. Methodology
Data Collection (custom dataset)
Data Preprocessing
Handling categorical values
Normalization
Splitting dataset (Training & Testing)
Model Training
Prediction
Evaluation
6. Implementation
Tools & Technologies:
Python
Pandas
NumPy
Scikit-learn
MLxtend
Sample Code
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression

df = pd.read_csv("student_data.csv")

X = df[['Study_Hours']]
y = df['Final_Exam_Score']

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)

model = LinearRegression()
model.fit(X_train, y_train)

predictions = model.predict(X_test)
7. Results
Multiple Linear Regression performed better than Simple Linear Regression
SVM and KNN gave high classification accuracy
Decision Tree provided easy interpretation
Naïve Bayes worked efficiently with less computation
8. Advantages
Helps predict student performance early
Improves placement preparation
Easy to implement
Useful for educational institutions
9. Limitations
Dataset size is small
Accuracy depends on data quality
Real-world data may vary
10. Applications
Student performance analysis
Placement prediction systems
Academic counseling
Educational analytics
11. Conclusion

This project successfully applied multiple Machine Learning algorithms to predict student performance and placement outcomes. The results show that factors like study hours, attendance, and internal marks significantly influence academic success.

Among all models, Multiple Linear Regression and SVM performed the best. This system can help institutions make data-driven decisions to improve student outcomes.
