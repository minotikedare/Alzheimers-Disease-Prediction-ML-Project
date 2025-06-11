# Alzheimers-Disease-Prediction-ML-Project by Dr Minoti Kedare

# Alzheimer's Disease Dataset

This machine learning project explores a dataset containing health information of 2,149 patients related to Alzheimer's Disease. The dataset includes demographic details, lifestyle factors, medical history, clinical measurements, cognitive assessments, and symptoms to support research and model development.

**Goal**: To develop a machine learning model to predict Alzheimer’s Disease diagnosis based on a diverse set of patient data. 

## Variables Description of the Dataset

### 1. Patient Information
- `PatientID`: Unique identifier for each patient

### 2. Demographic Details
- `Age`: Age of the patient (60 to 90 years)
- `Gender`: 0 = Male, 1 = Female
- `Ethnicity`:  
  - 0 = Caucasian  
  - 1 = African American  
  - 2 = Asian  
  - 3 = Other
- `EducationLevel`:  
  - 0 = None  
  - 1 = High School  
  - 2 = Bachelor's  
  - 3 = Higher

### 3. Lifestyle Factors
- `BMI`: Body Mass Index (15 to 40)
- `Smoking`: 0 = No, 1 = Yes
- `AlcoholConsumption`: Weekly alcohol consumption (0 to 20 units)
- `PhysicalActivity`: Weekly physical activity (0 to 10 hours)
- `DietQuality`: Score from 0 to 10
- `SleepQuality`: Score from 4 to 10

### 4. Medical History
- `FamilyHistoryAlzheimers`: 0 = No, 1 = Yes
- `CardiovascularDisease`: 0 = No, 1 = Yes
- `Diabetes`: 0 = No, 1 = Yes
- `Depression`: 0 = No, 1 = Yes
- `HeadInjury`: 0 = No, 1 = Yes
- `Hypertension`: 0 = No, 1 = Yes

### 5. Clinical Measurements
- `SystolicBP`: Systolic blood pressure (90 to 180 mmHg)
- `DiastolicBP`: Diastolic blood pressure (60 to 120 mmHg)
- `CholesterolTotal`: Total cholesterol (150 to 300 mg/dL)
- `CholesterolLDL`: LDL cholesterol (50 to 200 mg/dL)
- `CholesterolHDL`: HDL cholesterol (20 to 100 mg/dL)
- `CholesterolTriglycerides`: Triglycerides level (50 to 400 mg/dL)

### 6. Cognitive and Functional Assessments
- `MMSE`: Mini-Mental State Examination (0 to 30)
   Lower scores indicate more cognitive impairment.
- `FunctionalAssessment`: Functional score (0 to 10)
   Lower scores means more impairment.
- `MemoryComplaints`: 0 = No, 1 = Yes
- `BehavioralProblems`: 0 = No, 1 = Yes
- `ADL`: Activities of Daily Living (0 to 10)
   Lower scores show more impairment.

### 7. Symptoms
- `Confusion`: 0 = No, 1 = Yes
- `Disorientation`: 0 = No, 1 = Yes
- `PersonalityChanges`: 0 = No, 1 = Yes
- `DifficultyCompletingTasks`: 0 = No, 1 = Yes
- `Forgetfulness`: 0 = No, 1 = Yes

### 8. Diagnosis
- `Diagnosis`: 0 = No Alzheimer's, 1 = Alzheimer's diagnosis

### 9. Confidential
- `DoctorInCharge`: Confidential field marked as “XXXConfid” for all records

## Variables Used

#### Input Variable (Independent Variables)

Age, Gender, Ethnicity, BMI, Smoking, AlcoholConsumption, PhysicalActivity, DietQuality, FamilyHistoryAlzheimers, CardiovascularDisease, Diabetes, Depression, HeadInjury, Hypertension, MemoryComplaints, BehavioralProblems, Confusion, Disorientation, DifficultyCompletingTasks, Forgetfulness

#### Output Variable (Target)

Diagnosis - Indicates whether the patient has been diagnosed with Alzheimer’s Disease (0 = No, 1 = Yes)

## Preprocessing Steps
- Removed irrelevant features (e.g., PatientID, DoctorInCharge, MMSE)
- Checked for and confirmed absence of missing values or duplicates
- Detected and confirmed no significant outliers using Interquartile Range Method
- Assessed distribution using Shapiro-Wilk normality tests and Q-Q plots
- Performed Chi-square tests for statistical significance of categorical variables

## Models Used & Accuracy

| Model                | Accuracy (%) |
|---------------------|--------------|
| **Logistic Regression** | **73.95** |
| Random Forest       | 72.09        |
| CatBoost            | 70.93        |
| LightGBM            | 70.47        |
| XGBoost             | 66.98        |

- All models handled class imbalance using techniques such as `class_weight`, `auto_class_weights` and `scale_pos_weight`.


## Source and Citation
Dataset by Rabie El Kharoua, published on [Kaggle](https://www.kaggle.com/dsv/8668279).  
DOI: [10.34740/KAGGLE/DSV/8668279](https://doi.org/10.34740/KAGGLE/DSV/8668279) 

```bibtex
@misc{rabie_el_kharoua_2024,
  title={Alzheimer's Disease Dataset},
  url={https://www.kaggle.com/dsv/8668279},
  DOI={10.34740/KAGGLE/DSV/8668279},
  publisher={Kaggle},
  author={Rabie El Kharoua},
  year={2024}
} 
