# Hospital Readmission Prediction Project
## Introduction
In this final project, I aim to analyze synthetic hospital readmission data to develop predictive models using machine learning (ML) and artificial intelligence (AI) techniques. The dataset comprises 5,000 entries in the training set and 2,000 entries in the test set, with various fields such as age, gender, primary diagnosis, number of procedures, days in hospital, comorbidity score, discharge destination, and readmission status. By leveraging these data fields, I will employ ML and AI algorithms to predict the likelihood of patient readmission. This analysis will help identify key factors influencing readmission rates and enable healthcare providers to implement targeted interventions to reduce readmissions, ultimately improving patient outcomes and optimizing hospital resources.
## Research Question
Can we predict the likelihood of a patient being readmitted to the hospital within 30 days of discharge using patient demographics, clinical data, and hospitalization details?

## Expected Data Sources
The data will be sourced from a synthetic healthcare dataset containing 5,000 anonymized patient records with the following fields: age, gender, primary diagnosis, number of procedures, days in hospital, comorbidity score, discharge destination, and readmission status. https://www.kaggle.com/datasets/vanpatangan/readmission-dataset?resource=download

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


