# **Skimlit: NLP for Medical Abstract Classification**

This project replicates and extends the paper "*PubMed 200k RCT: a Dataset for Sequential Sentence Classification in Medical Abstracts*" using Natural Language Processing (NLP) techniques. It aims to classify medical abstract sentences into categories like **Background**, **Objective**, **Methods**, **Results**, and **Conclusions**, enabling easier and faster comprehension of medical research.

---

## **Project Overview**
The objective of this project is to build an NLP pipeline that:
- Processes medical abstracts from the **PubMed RCT dataset**.
- Classifies sentences into predefined categories.
- Incorporates both token-based and character-based deep learning models to improve classification accuracy.

This project leverages various deep learning models, including **Conv1D**, **LSTM**, **TensorFlow Hub Pretrained Embeddings**, and hybrid models combining token and character embeddings.

---

## **Dataset**
- **Source**: [PubMed RCT](https://github.com/Franck-Dernoncourt/pubmed-rct)
- **Data Structure**:
  - Training Set: 180,040 sentences
  - Validation Set: 30,212 sentences
  - Test Set: 30,135 sentences
- **Sentence Categories**:
  - **Background**
  - **Objective**
  - **Methods**
  - **Results**
  - **Conclusions**

---

## **Models Implemented**
### 1. **Baseline Model (Naive Bayes + TF-IDF)**
- Achieved validation accuracy: **72%**

### 2. **Conv1D Model**
- Token-based text classification.
- Validation accuracy: **78.9%**

### 3. **TensorFlow Hub Pretrained Embeddings**
- Uses Universal Sentence Encoder (USE) for token embeddings.
- Validation accuracy: **71.3%**

### 4. **Conv1D with Character-Level Embeddings**
- Processes sequences at the character level.
- Validation accuracy: **65.1%**

### 5. **Hybrid Model**
- Combines token-level and character-level embeddings.
- Achieved validation accuracy: **73.5%**

---

## **Project Highlights**
- **Data Preprocessing**:
  - Extracted and tokenized sentences.
  - One-hot encoded target labels.
  - Incorporated character-level embeddings for nuanced representation.
- **Deep Learning Techniques**:
  - Implemented **Conv1D**, **LSTM**, and **Bidirectional LSTM** models.
  - Explored **pretrained embeddings** for better semantic understanding.
- **Hybrid Approach**:
  - Combined token and character embeddings to leverage strengths of both.

---

## **Setup and Installation**
1. Clone the repository:
   ```bash
   git clone https://github.com/ShreCodes2809/skimlit.git
   cd skimlit
   ```
2.. Download the dataset from [PubMed RCT GitHub](https://github.com/Franck-Dernoncourt/pubmed-rct) and place it in the `data/` directory.

---

## **Results**
- **Baseline Model**:
  - Accuracy: **72%**
  - Precision: **71.8%**
  - Recall: **72.1%**
  - F1 Score: **69.9%**
- **Hybrid Model**:
  - Accuracy: **73.5%**
  - Precision: **73.1%**
  - Recall: **73.4%**
  - F1 Score: **72.9%**

---

## **Future Enhancements**
- Extend to additional datasets for improved generalization.
- Incorporate transformer models like BERT or GPT for better performance.
- Experiment with attention mechanisms to prioritize critical text parts.

---

## **Acknowledgments**
This project is inspired by the research paper *PubMed 200k RCT* and its accompanying dataset and codebase. Special thanks to TensorFlow and the NLP community for providing invaluable tools and resources.

---
