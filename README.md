**Healthcare Symptom Classification using Classical and Neural Models**

This project implements four different NLP-based models to classify healthcare symptom descriptions into disease groups. The original dataset contained 30 disease classes, but due to extremely high symptom overlap and lack of discriminative signal, the labels were restructured into 7 statistically derived disease groups. All models were trained, validated, and compared on this grouped label space.

The project includes:

- TF-IDF + Support Vector Machine (SVM)
- Feed-Forward Neural Network (FFNN)
- Simple Recurrent Neural Network (RNN)
- Long Short-Term Memory Network (LSTM)

**Dataset:**

Kaggle: Healthcare Symptoms to Disease Classification

https://www.kaggle.com/datasets/kundanbedmutha/healthcare-symptomsdisease-classification-dataset

**Preprocessing steps:**

- Symptom parsing and normalization
- Multi-hot encoding and integer sequence encoding
- TF-IDF text vectorization
- Disease grouping using agglomerative clustering

**Model Performance**

| Model               | Validation Accuracy | Test Accuracy |
|---------------------|----------------------|---------------|
| SVM (TF-IDF)        | 0.2733               | 0.2683        |
| FFNN (Multi-hot)    | 0.2733               | 0.2717        |
| RNN (Sequence)      | 0.2659               | 0.2661        |
| LSTM (Sequence)     | 0.2733               | 0.2717        |

All models converge to similar accuracy due to inherent dataset limitations and the constrained feature space.

**Features**

- Clean, modular, PEP8-compliant code
- Reproducible preprocessing and training pipeline
- Disease clustering to create a learnable label space
- Four fully implemented and comparable classification models

**Architecture**
<img width="1541" height="121" alt="Unknown" src="https://github.com/user-attachments/assets/ed24f0b0-4f66-485e-a885-cccae7acb4cd" />

**Report**

A 2-page technical report is included, containing methodology, evaluation, dataset analysis, and limitations.

**Authors**

Baker Huseyin

Islah Haoues
