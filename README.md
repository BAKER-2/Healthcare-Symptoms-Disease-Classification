## Healthcare Symptom Classification using Classical and Neural Models

This project implements four different NLP-based models to classify healthcare symptom descriptions into disease groups. The original dataset contains 30 disease classes, but due to extreme symptom overlap and a lack of discriminative signal, the original label space was not learnable. To address this limitation, the diseases were restructured into **four data-driven disease groups** using unsupervised clustering.

All models were trained, validated, and compared on this grouped label space. During inference, predictions are presented as a disease group along with the list of diseases belonging to that group, providing an interpretable differential diagnosis rather than a single disease prediction.

### Models Implemented

- TF-IDF + Support Vector Machine (SVM)
- Feed-Forward Neural Network (FFNN) using multi-hot symptom vectors
- Simple Recurrent Neural Network (RNN) using symptom sequences
- Long Short-Term Memory Network (LSTM) using symptom sequences

---

### Dataset

**Kaggle: Healthcare Symptoms to Disease Classification**

https://www.kaggle.com/datasets/kundanbedmutha/healthcare-symptomsdisease-classification-dataset

The dataset contains approximately 25,000 samples, 28 unique symptoms, and 30 original disease labels. Each sample includes between three and seven symptoms.

---

### Preprocessing and Label Engineering

- Symptom parsing, normalization, and tokenization
- TF-IDF vectorization of symptom text
- Multi-hot encoding of symptom presence
- Integer encoding and padding of symptom sequences
- Disease grouping using **k-means clustering (k = 6)** on disease-level symptom frequency vectors
- Reassignment of singleton clusters to nearest non-singleton centroids
- Final label space consisting of **four disease groups**

---

### Model Performance

| Model            | Validation Accuracy | Test Accuracy |
|------------------|---------------------|---------------|
| SVM (TF-IDF)     | 0.2851              | 0.2872        |
| FFNN (Multi-hot) | 0.2923              | 0.3008        |
| RNN (Sequence)   | 0.2931              | 0.3048        |
| LSTM (Sequence)  | 0.2947              | 0.3051        |

All models outperform the 25% random baseline for four classes. Neural and sequence-based models achieve modest but consistent improvements over the classical baseline.

---

### Features

- Clean, modular, PEP8-compliant code
- Reproducible preprocessing and training pipeline
- Data-driven disease grouping to create a learnable label space
- Four fully implemented and comparable classification models
- Interactive inference that outputs disease groups with associated disease lists

---

### Architecture

The architecture diagram illustrates the full prediction pipeline, from symptom input and preprocessing to parallel model inference and interpretable disease group output.

<img width="827" height="704" alt="healthcare_nlp_architecture drawio" src="https://github.com/user-attachments/assets/08defd8d-595e-41cd-9250-9fbec01abb82" />

---

### Report

A 2-page technical report is included, detailing methodology, clustering strategy, experimental results, dataset limitations, and critical analysis. The report is fully aligned with the implemented models and the live demo.

---

### Authors

- **Baker Huseyin**
- **Islah Haoues**
