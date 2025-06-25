# Quora Question Duplicate Detection with a Siamese Network ❓🔁❓

This repository contains the implementation of a project from the **DeepLearning.AI Natural Language Processing Specialization**. It demonstrates how to build and train a Siamese Network using TensorFlow to determine whether two questions are duplicates.

## 📘 Project Overview

The goal is to develop a model that can identify similar questions from the Quora Question Pairs dataset — a task essential for reducing redundant content in community forums and Q&A platforms.

The approach involves a **Siamese Network**, which processes both questions through shared neural network layers to project them into a high-dimensional vector space. The similarity between question pairs is evaluated using the cosine distance between their embeddings.

## 🧠 Technical Highlights & Key Concepts

- **Siamese Network Architecture:**
  - `TextVectorization` for tokenizing input text.
  - `Embedding` layer for dense vector representations.
  - `LSTM` layer to capture context and semantics.
  - `Lambda` layer to normalize output vectors.

- **Triplet Loss with Hard Negative Mining:**
  - Trained using a **Triplet Loss** function instead of standard binary classification loss.
  - Encourages closer embeddings for duplicates and separates non-duplicates.
  - Implements **hard negative mining** to improve learning by considering:
    - Closest negative sample.
    - Mean negative sample within each batch.

- **Evaluation Strategy:**
  - Uses **cosine similarity** to compare embeddings.
  - Classifies pairs as duplicates based on a similarity threshold (e.g., 0.7).
  - Evaluates model performance using **accuracy** and **confusion matrix** metrics.

## 🎓 Source & Acknowledgements

This project is part of **Course 3: Natural Language Processing with Sequence Models** in the  
[DeepLearning.AI Natural Language Processing Specialization](https://www.coursera.org/specializations/natural-language-processing) by Andrew Ng.

All credit for the original dataset, assignment, and instructional content goes to DeepLearning.AI and the course instructors.

---

> ✨ This project demonstrates how powerful distance-based architectures like Siamese Networks can be for semantic similarity tasks in natural language processing.
