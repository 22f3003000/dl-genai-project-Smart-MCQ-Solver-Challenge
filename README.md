# Smart MCQ Solver Challenge

An intelligent multiple-choice question-answering system developed for the Kaggle challenge. This system leverages advanced Natural Language Processing (NLP), Large Language Models (LLMs), and strategic answer ranking to predict and rank the top three most probable correct answers for complex multiple-choice questions.

**Author:** Debmalya Sanyal
**Student/Participant ID:** 22f3003000 

---

## 📌 Project Overview
Multiple-choice question answering serves as a critical benchmark for evaluating reasoning, language understanding, and answer-ranking capabilities in modern AI systems. In this competition, models are tasked with handling challenging MCQ-style questions. Each question includes a prompt and five potential choices (`A`, `B`, `C`, `D`, and `E`). 

The objective is to predict the top **three** most probable correct answers for each question, ranked by confidence.

### Evaluation Metric
Submissions are evaluated using **Mean Average Precision at 3 (MAP@3)**. This metric highly rewards models that place the true correct answer higher up in their top-3 predicted list:
- `A B C` $\rightarrow$ **Highest Score** (Correct answer is the 1st choice)
- `B A C` $\rightarrow$ **Lower Score** (Correct answer is the 2nd choice)
- `C D A` $\rightarrow$ **Lowest Score** (Correct answer is the 3rd choice)

---

## 📂 Project Repository Structure

```text
smart-mcq-solver-challenge/
│
├── data/                  # Raw and processed train/test datasets
│   ├── train.csv
│   └── test.csv
│
├── notebooks/             # Jupyter/Kaggle/Colab notebooks for EDA & prototyping
│   └── exploration_and_training.ipynb
│
├── scripts/               # Production-ready Python scripts for modular pipeline execution
│   ├── __init__.py
│   ├── data_loader.py     # Preprocessing and tokenization utils
│   ├── model.py           # Multiple-Choice model definitions
│   └── evaluate.py        # MAP@3 calculation and validation scripts
│
├── submissions/           # Generated submission files ready for Kaggle upload
│   └── submission.csv
│
├── requirements.txt       # Environment dependencies
└── README.md              # Project documentation
