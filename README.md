# Healthcare Data Entity Recognition Model

## Problem Statement

In this project, we consider a hypothetical example of a health tech company called ‘BeHealthy’. The goal is to connect medical communities with millions of patients across the country through a web platform. This platform allows doctors to list their services, manage patient interactions, book appointments, track past medical records, and provide e-prescriptions.

Companies like ‘BeHealthy’ generate vast amounts of medical data daily. Our task is to analyze this data and extract meaningful information, specifically identifying diseases and their treatments using Named Entity Recognition (NER).

Given a dataset containing medical text, our objective is to build a custom NER model to identify disease names and their probable treatments. The extracted information is then presented in a structured format, such as a dictionary or table.

## Approach

### 1. Data Preprocessing

- Construct sentences from individual words in the train_sent and test_sent datasets.
- Similarly, reconstruct label sequences in the train_label and test_label datasets.
- Print example sentences and label counts to ensure proper data preprocessing.

### 2. Concept Identification

- Use Part-of-Speech (PoS) tagging to identify and extract tokens labeled as NOUN or PROPN.
- Calculate the frequency of these tokens in the combined train and test datasets.
- Print the top 25 most common tokens with NOUN or PROPN tags.

### 3. Defining Features for CRF

- Define features for the CRF model, including PoS tags and preceding word information.
- Mark the beginning and end of sentences with appropriate features.

### 4. Getting Features and Labels of Sentences

- Write code to extract feature values for each sentence.
- Write code to generate a list of labels for each sentence.

### 5. Defining Input and Target Variables

- Extract feature values for each sentence as input variables for the CRF model.
- Extract labels as target variables for the CRF model.

### 6. Building the Model

- Build a Conditional Random Fields (CRF) model using the defined features and target variables.

### 7. Evaluating the Model

- Predict labels for each token in the test dataset using the CRF model.
- Calculate the F1 score to evaluate the model's performance.

### 8. Identifying Diseases and Predicted Treatments Using a Custom NER

- Create a dictionary where diseases are keys and treatments are values.
- Predict treatments for specific diseases, such as 'hereditary retinoblastoma'.

## Results

The model was evaluated using the F1 score, which measures the accuracy of the model in terms of precision and recall. Our CRF model achieved an impressive F1 score of 0.9059791628543951, indicating excellent performance in identifying and classifying entities in healthcare data.

## Conclusion

By leveraging the CRF model, we effectively identified and classified entities within healthcare data. This approach can significantly aid in extracting meaningful insights from medical texts, improving information retrieval, and supporting decision-making processes in the healthcare domain.

Feel free to explore the data, experiment with different features, and enhance the NER system's performance. For any questions mail to sreenu.winz@gmail.com

Thank you for following along with this project, and happy coding!
