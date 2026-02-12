# Model Card: Diabetes Readmission Prediction

## Intended Use

### Primary Use Cases
This model is intended to predict whether a hospitalized diabetic patient will be readmitted within 30 days of discharge. It should be used for:

* Educational and research purposes (binary classification, ML pipelines)  
* Exploratory analysis of clinical readmission risk patterns  
* Comparing different modeling approaches on tabular data  

This model is not designed for clinical decision support or any real-world medical diagnosis without professional oversight.

### Out-of-Scope Uses

* Making treatment or discharge decisions for actual patients  
* Direct use in hospital workflows without regulatory review  
* Use in systems that affect patient decisions  

## Evaluation Metrics

The task is binary classification of whether or not the patient is readmitted within 30 days, so the following metrics are recommended:  

* **Accuracy:** Overall correctness of the model's predictions  
* **Precision:** Fraction of correct positive predictions  
* **Recall:** Fraction of actual positives correctly identified  
* **F1 Score:** Mean of precision and recall  
* **ROC-AUC:** Shows trade-off between true positives and false positive rates  

## Limitations

* **Data Age & Scope:** The dataset covers records from 1999–2008 and may not reflect current clinical practice or patient demographics  
* **Sensitive Features:** Attributes like age, race, and gender are present and may correlate with readmission, which can introduce bias  
* **Missing Values & Data Quality:** Many fields have missing entries, requiring careful preprocessing and imputation  
* **Feature Representation:** Categorical variables with many levels complicate modeling and might need embedding or grouping  
* **Class Imbalance:** The proportion of readmitted vs. non-readmitted may be skewed, potentially degrading some metrics if not handled  

## Risks

* **Bias & Fairness:** Use of demographic information can lead to models that appear predictive but unfairly disadvantage groups. Bias assessment is recommended before any sensitive use  
* **Health Implications:** Misclassifications in a clinical context, especially false negatives, can have health implications if the model is misused  
* **Overgeneralization:** Good performance on this dataset does not imply real-world readiness. External validation on current clinical data is needed  
* **Privacy Awareness:** Even though the UCI dataset is anonymized, health data is sensitive. Always handle and share results responsibly  
