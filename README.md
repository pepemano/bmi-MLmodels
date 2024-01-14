The code reproduces a recent 'submitted scientific article' currently under consideration.

Title 
Enhancing BMI Predictions: A Machine Learning Approach

Abstract
This paper investigates the predictive capabilities of the Body Mass Index (BMI) formula over thousands of individuals. It explores the potential enhancements achievable through integrating additional parameters using machine learning (ML) models. After exploring a wide variety of modern ML models (K-Nearest Neighbors, Neural Networks, Decision Trees, Support Vector Classification, Logistic Regression, and Ridge Classifiers. Ensemble models: voting Classifier, Random Forest, and Gradient Boosting), most models demonstrated a high precision capability, and, interestingly, some models could either equalize or even perform better than the reference model. Our results suggest that incorporating into the conventional BMI formula variables, such as age or gender, may lead to more accurate and personalized BMI measurements, helping health practitioners provide more realistic weight management and health assessments and early diagnoses, treatments, and enhanced healthcare. 

Pre-steps:
  1. Download the input dataset (training/test set) from NHANES (https://www.cdc.gov/nchs/nhanes/index.htm)
  2. Extract data to be analyzed. In our case, we are interested in Age, Gender, Ethnicity, Weight, Height, and BMI values.
  3. Transform the Gender values from the previous set into numeric values, i.e. Female/Male (O male, 1 female)
  4. Transform the BMI values from the previous set into numerical class values (value column below) based on the following WHO criteria:
             BMI	Class            Value
          < 18.5	Underweight       -1
        18.5–24.9	Normal weight      0
        25.0–29.9	Pre-obesity       +1
        30.0–34.9	Obesity class I   +2
