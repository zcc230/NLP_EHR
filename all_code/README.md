Computational Phenotyping with HF patients using CNN

Data source: MIMIC3

#data used in code

ADMISSIONS.csv
DIAGNOSES_ICD.csv
PROCEDURES_ICD.csv
PRESCRIPTIONS.csv
PATIENTS.csv


#data for referencing ICD codes

D_ICD_DIAGNOSES.csv
D_ICD_PROCEDURES.csv

Programs:(run sequentially, make sure you correct directory for data)

Initial_data_preprocessing.ipynb -> load the data from raw mimic files to get all events for each patient

Create_date_token_feature.ipynb -> padding time token features into patients' event data

train_word2vec.ipynb -> train word2vec model using events data

filter_and_contruct_patient_groups.ipynb -> divide patients and filter out patients with legit amount of data/contruct demographic features

processingData * -> load the data and construct features for baseline models
baselineModels * -> train baseline prediction models

setup_train_visualize_cnn.ipynb => main body of the analysis
