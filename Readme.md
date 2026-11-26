# Predicting the presence of cardiovascular disease
**Course:** Fundamentals of Machine Learning  
**Project team:** Team 8 - Ariadna Lopez Traver, Daniel Moore Burgos, Alejandro Ucelayeta Jarque  
**Dataset:** [Cardiovascular Disease Dataset (Kaggle)](https://www.kaggle.com/datasets/sulianova/cardiovascular-disease-dataset?resource=download$0)

## 1. Project Objective & Problem Formulation
Cardiovascular diseases (CVDs) are a group of conditions affecting the heart and blood vessels, and are one of the leading causes of mortality globally.

The objective of this project is to build, evaluate, and analyze supervised binary classification models capable of predicting the presence or absence of CVDs drom clinical examination data, patient metrics, and lifestyle habits.

### Dataset features

The dataset consists of 70 000 records of patients data in 12 features, such as age, gender, systolic blood pressure, diastolic blood pressure, etc. The target class "cardio" equals to 1, when patient has cardiovascular desease, and it's 0, if patient is healthy.

There are 3 types of input features:
* Objective: factual information.
* Examination: results of medical examination.
* Subjective: information given by the patient.

| Feature | Variable Type | Variable | Value Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| Age | Objective Feature | `age` | int (days) | Patient's age in days |
| Height | Objective Feature | `height` | int (cm) | Patient's height |
| Weight | Objective Feature | `weight` | float (kg) | Patient's weight |
| Gender | Objective Feature | `gender` | categorical code | 1: women, 2: men |
| Systolic blood pressure | Examination Feature | `ap_hi` | int (mmHg) | Systolic blood pressure |
| Diastolic blood pressure | Examination Feature | `ap_lo` | int (mmHg) | Diastolic blood pressure |
| Cholesterol | Examination Feature | `cholesterol` | ordinal (1, 2, 3) | 1: normal, 2: above normal, 3: well above normal |
| Glucose | Examination Feature | `gluc` | ordinal (1, 2, 3) | 1: normal, 2: above normal, 3: well above normal |
| Smoking | Subjective Feature | `smoke` | binary | Self-reported smoking status |
| Alcohol intake | Subjective Feature | `alco` | binary | Self-reported alcohol intake |
| Physical activity | Subjective Feature | `active` | binary | Self-reported physical activity |
| Cardio (Target) | Target Variable | `cardio` | binary | Presence (1) or absence (0) of cardiovascular disease |

### Methodology and team workflow

To ensure methodological rigor, we follow the OSEMN workflow (Obtain, Scrub, Explore, Model, iNterpret).

The team uses an anti-leakage protocol, the dataset is split into training (80%) and test (20%) sets immediately after basic structural verification. All exploratory data analysis (EDA), outlier handling, feature engineering, scaling, and cross-validation will be performed exclusively on the training set.

A fixed gloval `RANDOM_SEED` is enforced across all splits and models to ensure reproducibility.

The team manages the project through a shared GitHub repository structured into *data/* (hosting the raw dataset) and *notebooks/* (hosting the master notebook, *Main_Pipeline.ipynb*). Using Google Colab integrated with GitHub allows all three members to run and update the notebook consistently from any machine, while a portable data loader (checking local paths first with the GitHub raw data fallback) ensures seamless execution.
