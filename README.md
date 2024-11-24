# Module 21 Challenge - SMS Spam Classification; Gradio Application

This project demonstrates the creation of a machine learning model to classify SMS messages as "spam" or "not spam." Using a linear Support Vector Classification (SVC) model and TF-IDF vectorization, the solution is deployed in an interactive Gradio application, allowing users to test text messages and receive feedback on whether the message is spam or not.

---

## Project Files

The project consists of the following files:
- **`gradio_sms_text_classification.ipynb`**: The main notebook containing the refactored code for SMS classification and the Gradio application.
- **`sms_text_classification_solution.ipynb`**: The starter solution file used as a reference to implement the final solution.
- **`SMSSpamCollection.csv`**: The dataset used to train the classification model.

---

## Project Features

### 1. SMS Classification Function
- Extracts:
  - **Features**: The `text_message` column from the dataset.
  - **Target**: The `label` column from the dataset.
- Splits the data into:
  - **Training Set**: 67% of the data.
  - **Testing Set**: 33% of the data.
- Builds a machine learning pipeline:
  - **TF-IDF Vectorizer**: Transforms text data into numerical features.
  - **Linear SVC**: Classifies messages as "spam" or "not spam."
- Trains the pipeline on the training data and returns the trained model.

### 2. SMS Prediction Function
- Predicts whether an SMS message is "spam" or "not spam" using the trained model.
- Provides user-friendly feedback:
  - For ham messages:  
    `"The text message: '{text}', is not spam."`
  - For spam messages:  
    `"The text message: '{text}', is spam."`

### 3. Gradio Interface Application
- Interactive web application for real-time SMS classification.
- Features:
  - **Input Textbox**: Users enter SMS text for classification.
  - **Output Textbox**: Displays the classification result ("spam" or "not spam").
  - **Labels**: Clear labels guide users for input and output.
- Generates a public URL for easy sharing and accessibility.

---