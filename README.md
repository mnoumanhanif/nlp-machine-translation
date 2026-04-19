# NLP Assignment: Sequence Modeling, RNNs & Seq2Seq Architecture

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![PyTorch](https://img.shields.io/badge/PyTorch-Framework-EE4C2C.svg)](https://pytorch.org/)
[![Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97-Datasets-orange.svg)](https://huggingface.co/docs/datasets/index)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

> **Author:** Muhammad Nouman Hanif (24K-8001)  
> **Course:** Natural Language Processing (NLP)

An advanced exploration of sequence modeling using PyTorch. This project progressively explores the mechanics of Recurrent Neural Networks (RNNs) on language modeling tasks and extends into complex sequence-to-sequence (Seq2Seq) architectures (including LSTM/GRU and Attention mechanisms) for machine translation.

---

##  Project Overview

This repository captures a deep dive into the evolution of neural sequence models, highlighting their strengths, mathematical bottlenecks (like vanishing gradients), and the strategies used to overcome them. The assignment is divided into major conceptual milestones:

1. **Vanilla RNN Language Modeling**
   - Training a Vanilla RNN from scratch on sequence data (e.g., WikiText-2).
   - Analyzing autoregressive sequence generation.
   - Diagnosing semantic drift, repetition, and the vanishing gradient bottleneck.
   - Evaluating generative capability using **Perplexity (PPL)** and Cross-Entropy Loss.

2. **Gated Architectures (LSTM & GRU)**
   - Understanding how information flow is mathematically regulated via distinct memory gates.
   - Comparing the representational power and computational efficiency of LSTMs versus GRUs.

3. **Sequence-to-Sequence (Seq2Seq) Machine Translation**
   - Designing Universal Encoder and Decoder classes.
   - Implementing neural machine translation pipelines natively using PyTorch.
   - Utilizing the **WMT14** dataset via Hugging Face datasets for training and validation.
   - Evaluating translation quality using the **BLEU** metric.

---

##  Repository Structure

\\\graphql
 NLP_Assignment.ipynb   # Main Jupyter Notebook
 report_v2.md           # Markdown version of the final analytical report
 report.tex             # LaTeX source for the formal project report
 report_body.tex        # LaTeX body content
 /images                # Visualizations, training loss curves, and diagrams
 requirements.txt       # Python dependencies required for the project
 .gitignore             # Configured to ignore Python/Jupyter artifacts
\\\

---

##  Getting Started

### Prerequisites

Ensure you have Python 3.8+ installed. It is highly recommended to use a virtual environment (\.venv\ or \conda\). A GPU capable of CUDA acceleration will dramatically speed up the Seq2Seq training.

### Installation

1. Clone the repository:
   \\\ash
   git clone https://github.com/your-username/nlp-sequence-modeling.git
   cd nlp-sequence-modeling
   \\\

2. Activate your virtual environment and install dependencies:
   \\\ash
   pip install -r requirements.txt
   \\\
   *(If \
equirements.txt\ is missing specific libraries, ensure \	orch\, \	ransformers\, \datasets\, \
umpy\, and \matplotlib\ are installed).*

### Execution

1. Launch Jupyter Notebook or VS Code to interact with the project:
   \\\ash
   jupyter notebook NLP_Assignment.ipynb
   \\\
2. Run the cells sequentially to reproduce the data preprocessing, model instantiations, training loops, and final evaluations.

---

##  Evaluation & Metrics

- **Language Modeling Phase:** Evaluated primarily on **Perplexity**. Lower perplexity reflects a model uniquelyपरशन of assigning high probabilities to true structural natural language elements.
- **Machine Translation Phase:** Evaluated using **BLEU** scores against the validation splits of standard corpora (e.g., WMT14), balancing n-gram precision against sequence length penalties.

---

##  Formal Report

A detailed analytical breakdown of the results, hyperparameter choices, sequence quality discussions, and architectural comparisons can be found in \
eport_v2.md\ and compiled from \
eport.tex\.

---
*Created as part of an academic deep-dive into Neural sequence computation and generation paradigms.*
