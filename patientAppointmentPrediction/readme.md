# What Has Been Done in This Study?
  1. **Data Engineering**: deal with duplicated items, useless features, value normalize, null value and illeagle value
  2. **Explore Data Analysis(EDA)**: understand the dataset and part of data interpretability.
  3. **Models Selection**: (i) Logistic Regression (ii) Decision Tree (iii) Random Forest

# Introductoin
## Background
Patients make appointments at clinics or hospitals to be checked by a doctor. Some of the patients do not show up for their appointments. This results in loss of valuable resources in terms of physician time and staffing allocation which could have been used more productively.

## The goal
The primary goal of this research is to find the suitable michine learning mode for predicting patient showing or not on the appointed date. Finally, apply it to improve medical resource utilization.

## The data
The original datasets from Kaggle (datasets: https://www.kaggle.com/datasets/joniarroba/noshowappointments/data).

  **01 - PatientId**: Identification of a patient

  **02 - AppointmentID**: Identification of each appointment

  **03 - Gender**: Male or Female . Female is the greater proportion, woman takes way more care of they health in comparison to man.

  **04 - DataMarcacaoConsulta**: The day of the actuall appointment, when they have to visit the doctor.

  **05 - DataAgendamento**: The day someone called or registered the appointment, this is before appointment of course.

  **06 - Age**: How old is the patient.

  **07 - Neighbourhood** : Where the appointment takes place.

  **08 - Scholarship**: True of False . Observation, this is a broad topic, consider reading this article https://en.wikipedia.org/wiki/Bolsa_Fam%C3%ADlia

  **09 - Hipertension**:   True or False

  **10 - Diabetes**:   True or False

  **11 - Alcoholism**:   True or False

  **12 - Handcap**:   True or False

  **13 - SMS_received**:   1 or more messages sent to the patient.

  **14 - No-show**: True(not showing) or False(showing).


## Prediction task
The goal in this dataset is to predict patient showing or not on the appointed date.


## Key Findings

**1. Model Findings**

Logistic Regression has the highest accuracy (80%), and Decision Tree has the lowest accuracy (73%). Combing other metrics, Logistic Regression has the best performace comparing Decision Tree and Random Forest.

**2. Correlationship Findings**

* Age has great relationship with Hipertension and Diabetes.
* Hipertension and Diabetes has close correlationship.
* No-showing has great correlationship with SMS_received and Scholarship.
* Showing has great correlationship with age.
* Number of showing patients from specific neighbourhood affected by receving SMS and ages.
* Number of showing patients without reciving sms is greater than showing patients with reciving sms, which mean that sending sms reminding is working.
* No clear correlation between showing and gender, chronic diseases.

