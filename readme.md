# Hospital Readmission Prediction Project
## Introduction
In this final project, I aim to analyze synthetic hospital readmission data to develop predictive models using machine learning (ML) and artificial intelligence (AI) techniques. The dataset comprises 5,000 entries in the training set and 2,000 entries in the test set, with various fields such as age, gender, primary diagnosis, number of procedures, days in hospital, comorbidity score, discharge destination, and readmission status. By leveraging these data fields, I will employ ML and AI algorithms to predict the likelihood of patient readmission. This analysis will help identify key factors influencing readmission rates and enable healthcare providers to implement targeted interventions to reduce readmissions, ultimately improving patient outcomes and optimizing hospital resources.
## Research Question
Can we predict the likelihood of a patient being readmitted to the hospital within 30 days of discharge using patient demographics, clinical data, and hospitalization details?

## Expected Data Source
The data will be sourced from a synthetic healthcare dataset containing 5,000 anonymized patient records with the following fields: age, gender, primary diagnosis, number of procedures, days in hospital, comorbidity score, discharge destination, and readmission status. https://www.kaggle.com/datasets/vanpatangan/readmission-dataset?resource=download

Extra resource: EDA and ML AI prediction component non graded combined notebook: https://www.kaggle.com/code/andrefft/notebook6bc63b787a 
## Hospital Readmission Prediction Techniques Expected to Use in Analysis
1. **Classification Algorithms**: Logistic Regression, Decision Trees, and Gradient Boosted Trees to predict readmission likelihood.
2. **Feature Engineering**: Use domain knowledge to transform fields (e.g., group primary diagnosis into broader categories) and assess variable importance.
3. **Dimensionality Reduction**: Principal Component Analysis (PCA) to identify and focus on the most impactful features.
4. **Deep Learning Models**: Recurrent Neural Networks (RNNs) to leverage sequential relationships if time-sequenced data such as patient histories are integrated.

## Use of Dataset Fields in the Analysis
- **Age**: Categorical or continuous predictor for readmission risk (e.g., older patients may have higher readmission risks).
- **Gender**: Analyze potential disparities in readmission risks.
- **Primary Diagnosis**: Group diagnoses into broader categories for analysis and identify conditions strongly associated with readmissions.
- **Number of Procedures**: Higher procedure counts may indicate complex cases with elevated risks.
- **Days in Hospital**: Longer stays may indicate more severe conditions, impacting readmission likelihood.
- **Comorbidity Score**: A higher score indicates greater patient complexity and likely higher readmission risks.
- **Discharge Destination**: Insights into care transitions (e.g., home vs. rehabilitation facility) and their impact on outcomes.
- **Readmitted (Target Variable)**: Binary outcome variable indicating if a patient was readmitted within 30 days.

## Expected Results
The analysis aims to deliver a predictive model that identifies patients at high risk of readmission with sufficient accuracy and reliability for real-world application. Additionally, it will uncover key patterns, such as which combinations of factors (e.g., diagnosis and comorbidity score) most strongly influence readmission risk.

## Why This Question Is Important
Hospital readmissions represent significant challenges, including financial penalties for providers under programs like CMS's Readmissions Reduction Program, and suboptimal outcomes for patients. If this question is left unaddressed:
- High-risk patients may not receive preventive care, resulting in worse health outcomes and increased healthcare costs.
- Hospitals may continue to face financial strain and reputational damage due to excessive readmissions.

The analysis will provide healthcare professionals with actionable insights, such as:
1. **Targeted Interventions**: Identify patients needing enhanced post-discharge support, such as care coordination or follow-up calls.
2. **Resource Optimization**: Allocate resources (e.g., additional nursing or case management) to high-risk areas to reduce readmissions.
3. **Policy Development**: Use insights to refine discharge planning and implement proactive care strategies.

By translating complex data into clear, actionable intelligence, this project ensures better resource utilization, improved patient outcomes, and cost-effective care delivery.


## 24.1 Capstone Nontechnical Report 
#### Business Understanding of the Problem
The objective of this analysis is to predict hospital readmissions within 30 days using a synthetic healthcare dataset. Hospital readmissions are costly and represent poor health outcomes for patients. Identifying patients at high risk of readmission allows healthcare providers to take preventive measures, reduce healthcare costs, and improve patient outcomes. By leveraging machine learning techniques, the aim is to predict the likelihood of readmission and uncover the key factors driving this risk.

#### Data Cleaning and Preprocessing
To ensure the accuracy and reliability of the models, the dataset underwent extensive cleaning and preprocessing, which included:
- Handling missing values.
- Converting categorical variables into appropriate formats (e.g., one-hot encoding for categorical features).
- Normalizing continuous variables to ensure consistent scale across the features.
- Addressing the class imbalance using techniques like oversampling to improve the model's ability to predict the minority class (readmitted).

#### Descriptive and Inferential Statistics
Descriptive statistics revealed that the dataset was highly imbalanced, with the majority of patients not being readmitted. The following key insights were derived:
- The average age of patients in the dataset was **53** years, with a higher proportion of older patients at risk for readmission.
- The comorbidity score, which accounts for additional health complications, showed that patients with higher scores had an increased likelihood of readmission.
- The average length of hospital stay was **7** days, with longer stays correlating with higher readmission risk.

Inferential statistics, such as correlation analysis and hypothesis testing, further reinforced these insights and highlighted significant relationships between patient characteristics and readmission likelihood.

#### Key Findings

After testing multiple machine learning models, the **Random Forest** model was identified as the most effective for predicting readmissions. Below are the key findings regarding feature importance:

1. **Strong Features for Predicting Readmission**:
   - **Age**: Older patients are at higher risk of readmission.
   - **Comorbidity Score**: Patients with more complex medical histories are more likely to be readmitted.
   - **Days in Hospital**: Patients with longer hospital stays tend to have more severe conditions and are more likely to be readmitted.
   - **Number of Procedures**: A higher number of procedures increases readmission likelihood, suggesting these patients may require more intensive treatment or recovery.

2. **SHAP Analysis**:
   In addition to feature importance, SHAP values provided deeper insights into the factors influencing the model's predictions. These features had a substantial impact on the model's output:
   - **Discharge to Rehabilitation Facility**: Patients discharged to rehabilitation facilities showed a higher likelihood of readmission due to complex care needs post-discharge.
   - **Kidney Disease**: Patients with kidney disease exhibited significantly higher readmission risks, highlighting the chronic nature and complications of the condition.
   - **Discharge to Home Healthcare**: Discharge to home healthcare was associated with higher readmission rates, emphasizing the need for intensive home care after discharge.
   - **Nursing Facility Discharge**: Similar to rehab facility discharges, patients transferred to nursing facilities were at an increased risk of readmission.
   - **Chronic Conditions (Diabetes, Hypertension, and Heart Disease)**: These conditions were strongly linked to higher readmission rates, stressing the need for effective management of chronic diseases to reduce hospital readmissions.

#### Actionable Insights for the Healthcare provider:

Based on the findings, the following actionable steps can be recommended for healthcare providers:
- **Targeted Post-Discharge Care**: Focus on patients who are older, have higher comorbidity scores, or have longer hospital stays for more intensive post-discharge monitoring and care.
- **Care Coordination for Chronic Conditions**: Prioritize patients with kidney disease, diabetes, hypertension, and heart disease for comprehensive follow-up care to manage these chronic conditions effectively.
- **Enhanced Discharge Planning**: Implement tailored discharge plans for patients discharged to rehabilitation facilities, home healthcare, or nursing facilities to ensure adequate care and minimize the risk of readmission.
- **Predictive Alerts**: Develop predictive systems using the identified features (age, comorbidity score, procedures, etc.) to alert healthcare teams about patients at high risk of readmission, enabling proactive interventions.

#### Next Steps and Recommendations
- **Model Refinement**: Experiment with additional techniques such as ensemble models or deep learning to further improve model performance.
- **More Data**: The model could benefit from incorporating more data points, including time-sequenced data such as patient history, to capture long-term trends in readmission risk.
- **Implementation in Real-World Settings**: Consider integrating the predictive model into a hospital's electronic health record system to provide real-time alerts to healthcare providers when patients are at high risk of readmission.


