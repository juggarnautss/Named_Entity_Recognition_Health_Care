# BeHealthy Medical Data Processing - Name Entity Recognition

## Problem Statement

‘BeHealthy’ has a web platform that allows doctors to list their services, manage patient interactions, and provide services for patients such as booking interactions with doctors and ordering medicines online. Here, doctors can easily organize appointments, track past medical records, and provide e-prescriptions.

‘BeHealthy’ provides medical services, prescriptions, and online consultations, generating large amounts of data daily.

### Example of Medical Data

Consider the following snippet of medical data that may be generated when a doctor is writing notes to a patient or reviewing a therapy: 
> “The patient was a 62-year-old man with squamous cell lung cancer, which was first successfully treated by a combination of radiation therapy and chemotherapy.”

In this dataset, diseases and their related treatments are often mentioned implicitly. For example, in the sentence above, the disease mentioned is "lung cancer," and its treatment can be identified as "chemotherapy."

### Goal

The goal is to build an algorithm to map diseases to their respective treatments from such datasets, despite the information being implicitly mentioned.

## Methodology

### Steps Followed

1. **Process and Modify Data:**
   - Convert the data into sentence format. This step is applied to the `train_sent` and `train_label` datasets and the test datasets.

2. **Define Features:**
   - Identify the features to build the Continuous Random Field (CRF) model.

3. **Apply Features:**
   - Apply the defined features to each sentence in the train and test datasets to get the feature values.

4. **Define Target Variable:**
   - Define the target variable once the features are computed.

5. **Build the CRF Model:**
   - Train the CRF model using the training dataset.

6. **Evaluate the Model:**
   - Perform the evaluation using a test dataset.

7. **Create Dictionary:**
   - Create a dictionary in which diseases are keys and treatments are values.

### Contributor
   - Sirin Shaikh