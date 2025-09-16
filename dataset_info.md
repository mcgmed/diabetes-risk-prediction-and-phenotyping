### Dataset Definition: Glycemic Control in Diabetes Mellitus Patients

**This study analyzes the glycemic control status of newly diagnosed diabetes mellitus patients in Istanbul three years after their initial diagnosis, with the goal of identifying key predictive factors.** The dataset was compiled from the national electronic health record system, e-Nabız, utilizing data from Istanbul province due to its higher data quality.

**Patient Population**

The study identified individuals in Istanbul who were newly diagnosed with diabetes mellitus in 2017. The criteria for a diabetes diagnosis included one of the following:

*   An existing diagnosis of diabetes (ICD-10 codes E10-E14).
*   A prescription for antidiabetic medications (excluding metformin).
*   An HbA1c level greater than 6.5%.

All selected patients had at least four HbA1c measurements (approximately one per year), as well as initial serum creatinine and lipid profile data.

**Data Collection**

For each patient, 105 variables were extracted from the e-Nabız system. These variables, which serve as independent variables in the study, were recorded either at the time of diagnosis or within the first year. They include:

*   Demographics (age at diagnosis, sex).
*   Initial laboratory results (serum HbA1c, lipid profile, creatinine).
*   The change in HbA1c levels between the initial measurement and the measurement at approximately 12 months.
*   Comorbidities (44 variables, indicating the presence or absence of other diseases within the first year of diagnosis).
*   Medications (52 variables, indicating the total dose of antidiabetics in the first year and the prescription of other drugs).

Comorbidities are classified using ICD-10 codes, while medications are classified using ATC codes. The dataset was cleaned to remove any noisy, extreme, or irrational values, and patients with missing data were excluded.

**Outcome Variable**

The primary outcome of the study, or the dependent variable, is **Glycemic_control**. This variable categorizes patients based on their HbA1c levels three years after their initial diagnosis. The categories are:

*   **Under control (0):** The last two recorded HbA1c values are below 7%.
*   **Poor control (1):** The last two recorded HbA1c values are not under 7%.

**Ethical Approval**

The study received ethical approval from the Akdeniz University Clinical Research Ethical Committee.

### Variable Definitions

Below is a clear and organized list of the variables included in the dataset:

**Patient Identifier**

*   **id:** Unique patient identification number.

**Demographics**

*   **sex:** Sex of the patient (1: female, 2: male).
*   **age:** Age of the patient at the time of diagnosis (in years).

**Laboratory Measurements at Diagnosis**

*   **HbA1c:** Serum HbA1c level at diagnosis (%).
*   **LDL:** Low-density lipoprotein level at diagnosis (mg/dL).
*   **Cholesterol:** Total cholesterol level at diagnosis (mg/dL).
*   **HDL:** High-density lipoprotein level at diagnosis (mg/dL).
*   **Creatinine:** Serum creatinine level at diagnosis (mg/dL).
*   **Triglyceride:** Triglyceride level at diagnosis (mg/dL).

**Change in HbA1c**

*   **Hba1c_change:** Percentage change in HbA1c from diagnosis to the first year.

**Comorbidities (Present in the first year of diagnosis)**

This is a series of binary variables where **1** indicates the presence of the condition and **0** indicates its absence.

*   **infectious_diseases**
*   **Malign_neoplasms**
*   **Obesity**
*   **Thyroid_dis**
*   **neoplasms_unknown**
*   **anemia**
*   **vitamin_deficiency**
*   **lipoprotein_met_dis**
*   **hematologic_dis**
*   **endocrine_other**
*   **bipolar_affective_dis**
*   **depression**
*   **anxiety_dis**
*   **Other_mental_dis**
*   **neuropathies**
*   **diabetic_nueropathy**
*   **nervous_sys_dis**
*   **cataract**
*   **retinopathy**
*   **refraction_dis**
*   **impacted_cerumen**
*   **tinnitus_h93_1**
*   **eye_other**
*   **otitis_externa_h60**
*   **mastoid_h60_h95**
*   **hypertension_i10**
*   **ischemic_heart_dis**
*   **cardiomyopathies**
*   **cerebrovascular**
*   **other_circulatory**
*   **respiratory_sys**
*   **oral_dis**
*   **gastro_oes_reflux**
*   **dyspepsia**
*   **digestive_sys_dis**
*   **skin_dis**
*   **musculoskeletal_dis**
*   **nephropaties**
*   **kidney_failure**
*   **other_genitourinary**
*   **pregnancy**
*   **birth**
*   **ceserian_multiple**
*   **other_pregnancy**

**Medications (Prescribed in the first year of diagnosis)**

These are also binary variables where **1** indicates the medication was prescribed and **0** indicates it was not.

*   **digestive_drugs**
*   **antiobesity**
*   **other_digestive**
*   **hematologic_drugs**
*   **cardiovascular_drugs**
*   **lipid_modifying**
*   **dermatologic_drugs**
*   **gynecologic_drugs**
*   **sex_hormones**
*   **systemic_hormones**
*   **glucagon**
*   **calcium_homeostasis_drugs**
*   **antiinfectives**
*   **vaccines**
*   **antineoplastics**
*   **endocrin_drugs**
*   **immunostimulants**
*   **immunosupresants**
*   **musculosceletal_drugs**
*   **anesthetics**
*   **analgesics**
*   **antiepileptics**
*   **antiparkinson**
*   **antipsychotics**
*   **anxiolytics**
*   **pshycoanaleptics**
*   **other_nervous_drugs**
*   **antiparasitic**
*   **respiratory_sys_drugs**
*   **eye_ear_drugs**
*   **various_drugs**

**Prescribed Amount of Antidiabetic Medications (in the first year after diagnosis)**

*   **akarboz; dapagliflozin; eksenatid; gliklazid; glimepirid; glipizid; linagliptin; nateglinid; pioglitazon_hcl; repaglinide; saksagliptin; sitagliptin; vildagliptin:** Prescribed amount in grams per year.
*   **insulin_aspart; insulin_detemir; insulin_glarjin; insulin_glusilin; insulin_lispro; insulin_nph; insulin_reguler:** Prescribed amount in 1000 IU per year.
*   **metformin_hcl:** Prescribed amount in kilograms per year.

**Dependent Variable**

*   **Glycemic_control:** The patient's glycemic control status three years after diagnosis (0: Under control, 1: Poor control).

### Dataset Citation:
Gulkesen, Kemal Hakan; Ülgü, Mustafa Mahir; Mutlu, Begum; Akünal, Abdullah; Ayvalı, Mustafa Okan; Akyürek, Özen; Birinci, Şuayip; Balcı, Mustafa Kemal; Sezer, Ebru (2024), “Machine Learning for Prediction of Glycemic Control in Diabetes Mellitus”, Mendeley Data, V2, doi: 10.17632/rr4rzzrjfc.2
