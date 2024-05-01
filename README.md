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

Post-steps:
  1. The code (ClassificationAGEth.ipynb) represents the experiment regarding the use of age, gender, and ethnicity as additional parameters to be compared to the only use of height and weight (traditional BMI formula).
  2. The code (ClassificationAGEth.ipynb) should be adapted to the other parameters to be studied. In our case, Height+Weight+Age+Gender+Ethnicity (same code here), H+W+Age (code to be adapted accordingly), H+W+Gender (to be adapted), H+W+Ethnicity (to be adapted), and H+W+Age+Gender (to be adapted). Plus the reference set Height(H)+Weight(W).
  3. The graphic (ClassificationAGEth.ipynb) combines the results from all the parameters under study. It requires some manual adaptation before producing the output.

Published Results:

. Reinventing the Body Mass Index: A Machine Learning approach (https://www.medrxiv.org/content/10.1101/2024.04.26.24306457v1)
