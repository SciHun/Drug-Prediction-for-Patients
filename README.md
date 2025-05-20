Drug Prediction for Patients using Machine Learning

This repository contains a machine learning model developed to predict the most appropriate drug treatment for patients based on their clinical and biochemical profiles. The model leverages patient data—comprising 18 key biochemical parameters (such as glucose, urea, creatinine, ALT, AST, CRP, hemoglobin, etc.)—to predict potential diseases and recommend drug treatments accordingly.

The dataset includes 2,900 patient records, each labeled with one of the following disease classes:

Class 0: Renal Failure,
Class 1: Anemia,
Class 2: Diabetes,
Class 3: Hypercholesterolemia,
Class 4: Hyperthyroidism,
Class 5: Hypothyroidism,
Class 6: Heart Attack,
Class 7: Pneumonia,
Class 8: Healthy

This is a retrospective study, and we used anonymized patient records collected from January 1, 2020, to June 1, 2024. The study was approved by the Ethics Committee of Atatürk University Research Hospital, and all necessary ethical permissions were obtained.

The project was conducted in collaboration with my last-term pharmacy student, Cansu Çelik.

A classification model was implemented using Python and TensorFlow. The core model is a Deep Neural Network (DNNClassifier) trained to accurately predict the disease class from the input biochemical data and subsequently map it to an appropriate drug recommendation, based on clinical pharmacological guidelines.

After disease classification, our model suggests drug recommendations tailored to each predicted disease class by analyzing the patient's biochemical and clinical parameters. The recommendations are rule-based and informed by standard clinical guidelines:

Class 0 – Renal Failure: Suggested treatments include ACE inhibitors (e.g., Enalapril), ARBs, phosphate binders, and erythropoiesis-stimulating agents, depending on creatinine, urea, potassium, and hemoglobin levels.
Class 1 – Anemia: Recommended therapies include oral or IV iron supplements (e.g., Ferrous Sulfate), Vitamin B12, or Erythropoietin depending on the anemia type (iron-deficiency, megaloblastic, etc.).
Class 2 – Diabetes: Recommended medications include Metformin, Insulin, DPP-4 inhibitors, or SGLT2 inhibitors, guided by glucose, HbA1c, and kidney function parameters.
Class 3 – Hypercholesterolemia: Suggested drugs are Statins (e.g., Atorvastatin, Rosuvastatin), possibly combined with Ezetimibe or PCSK9 inhibitors based on LDL-C and total cholesterol levels.
Class 4 – Hyperthyroidism: Recommended treatments include Antithyroid drugs (e.g., Methimazole or Propylthiouracil), and in some cases beta-blockers for symptom control.
Class 5 – Hypothyroidism: Standard therapy includes Levothyroxine, with dosage adjusted based on TSH and free T4 levels.
Class 6 – Heart Attack (Myocardial Infarction): Drug recommendations include Aspirin, Clopidogrel, Beta-blockers, ACE inhibitors, and Statins, depending on troponin, ECG data, and blood pressure.
Class 7 – Pneumonia: Empirical antibiotics are suggested, such as Amoxicillin-clavulanate, Azithromycin, or Ceftriaxone, tailored to CRP, WBC count, and radiological findings.
Class 8 – Healthy: No drug recommendation; patient is advised to continue routine health monitoring and preventive care.

Check out the full code, notebooks, and project details here:
🔗 https://github.com/SciHun/Drug-Prediction-for-Patients
