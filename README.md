🧠 Drug Prediction for Patients using Machine Learning
This repository contains a machine learning model developed to predict the most appropriate drug treatment for patients based on their clinical and biochemical profiles. The system integrates data-driven healthcare and artificial intelligence to support decision-making in personalized medicine.

📊 Project Overview
The model utilizes 2,900 anonymized patient records, each containing 18 critical biochemical parameters such as:

Glucose
Urea
Creatinine
ALT (Alanine Transaminase)
AST (Aspartate Transaminase)
CRP (C-Reactive Protein)
Hemoglobin
TSH
WBC (White Blood Cell count) and others relevant to disease diagnosis.

These parameters are used to predict a disease class and provide drug recommendations based on clinical pharmacological guidelines.

🏥 Study Design
Type of Study: Retrospective
Data Source: Patient records from Atatürk University Research Hospital
Study Period: January 1, 2020 – June 1, 2024
Ethical Approval: Approved by the Ethics Committee of Atatürk University Research Hospital
All necessary ethical permissions were obtained prior to data analysis.

👩‍🔬 This study was conducted in collaboration with my last-term pharmacy students, Cansu Çelik and Berivan Aslan.

🧬 Disease Classification
Each patient record is labeled with one of the following 9 disease classes:

Class	Disease
0	Renal Failure
1	Anemia
2	Diabetes
3	Hypercholesterolemia
4	Hyperthyroidism
5	Hypothyroidism
6	Heart Attack
7	Pneumonia
8	Healthy

🤖 Technical Implementation
Programming Language: Python
Framework: TensorFlow
Model: Deep Neural Network (DNNClassifier)
Purpose: Multiclass classification of diseases and drug recommendation mapping
The DNNClassifier model was trained using normalized biochemical parameters as input features. It outputs a predicted disease class label, which is then used to generate rule-based drug recommendations.

💊 Drug Recommendation System
After the disease is predicted, the model provides personalized drug suggestions based on standard clinical treatment protocols. Recommendations are tailored to the patient’s biochemical state and associated disease class:

🔹 Class 0 – Renal Failure
Drugs: ACE inhibitors (e.g., Enalapril), ARBs, Phosphate binders, Erythropoiesis-stimulating agents
Based on: Elevated creatinine, urea, electrolyte imbalance, and low hemoglobin
🔹 Class 1 – Anemia
Drugs: Ferrous sulfate (oral/IV), Vitamin B12, Erythropoietin
Based on: Low hemoglobin, hematocrit, and iron indices
🔹 Class 2 – Diabetes
Drugs: Metformin, Insulin, DPP-4 inhibitors, SGLT2 inhibitors
Based on: Elevated glucose, HbA1c (if available), and renal function
🔹 Class 3 – Hypercholesterolemia
Drugs: Statins (e.g., Atorvastatin), Ezetimibe, PCSK9 inhibitors
Based on: High total cholesterol, LDL levels
🔹 Class 4 – Hyperthyroidism
Drugs: Methimazole, Propylthiouracil, Beta-blockers (e.g., Propranolol)
Based on: Suppressed TSH, elevated free T4 or T3
🔹 Class 5 – Hypothyroidism
Drugs: Levothyroxine
Based on: Elevated TSH, low free T4
🔹 Class 6 – Heart Attack (Myocardial Infarction)
Drugs: Aspirin, Clopidogrel, Beta-blockers, ACE inhibitors, Statins
Based on: Elevated troponin, ECG data, abnormal CRP, and blood pressure values
🔹 Class 7 – Pneumonia
Drugs: Empirical antibiotics – Amoxicillin-clavulanate, Azithromycin, or Ceftriaxone
Based on: High CRP, WBC count, fever, and clinical signs (if available)
🔹 Class 8 – Healthy
Recommendation: No drug suggested; patient considered clinically normal. Routine monitoring advised.
## 💡 Authors
🔬 Harun Un, PhD – Clinical Biochemist & Data Scientist
🔬 Cansu Celik, BSc – Pharmacist 
🔬 Berivan Aslan, BSc – Pharmacist
