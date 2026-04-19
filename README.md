# Neural Sequence Modeling & Machine Translation

An empirical implementation and comparative analysis of Neural Machine Translation (NMT) architectures, tracing the evolution from baseline Recurrent Neural Networks to dynamic Attention mechanisms. 

This repository documents the progressive circumvention of the "Information Bottleneck" in sequence-to-sequence mappings, translating English contexts into structured German outputs.

## 🚀 Architectures Implemented
All models were implemented from scratch to mathematically evaluate their handling of long-context dependencies and gradient flows:
* **Vanilla RNNs:** Autoregressive context generation and vanishing gradient demonstrations.
* **Gated Architectures (LSTM & GRU):** Structured memory retention and temporal dependency tracking over sliding windows.
* **Seq2Seq Encoder-Decoder:** Multi-lingual mappings bridging English (Multi30k) to German.
* **Attention Mechanisms:** * Additive (Bahdanau)
    * Multiplicative (Luong)
    * Scaled Dot-Product Attention

## 📊 Empirical Results
The models were evaluated using BLEU, BERTScore, and METEOR metrics on the WMT14 (de-en) dataset subset. The integration of Scaled Dot-Product Attention with a GRU backbone yielded the highest performance, effectively solving the context decay problem inherent in long sequences.

| Model Architecture | BLEU | BERTScore | METEOR |
| :--- | :--- | :--- | :--- |
| Seq2Seq RNN (Baseline) | 0.00 | 52.91 | 6.66 |
| Seq2Seq LSTM | 0.30 | 54.56 | 9.63 |
| Seq2Seq GRU | 0.67 | 56.88 | 11.88 |
| GRU + Scaled Dot Attention | **3.42** | **64.30** | **19.93** |

## 🧠 Key Insights & Error Analysis
* **The Baseline Failure:** Traditional Encoder-Decoder setups suffered from catastrophic forgetting on sequences exceeding 20 tokens, dropping BLEU scores near zero.
* **The Attention Leap:** Attention dynamically calculates context vectors bypassing recurrent memory bottlenecks, leading to a 5x jump in BLEU and significant improvements in semantic survival (BERTScore).

## 🛠️ Tech Stack
* PyTorch (Custom neural layers and backpropagation)
* TorchText (Data pipelines)
* Multi30k / WMT14 Datasets
* Numpy & Matplotlib (Attention visualization heatmaps)
