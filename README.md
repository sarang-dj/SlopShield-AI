# SlopShield-AI
# 🤖 AI Slop Detector

### Detect AI-generated text with Transformers

**AI Slop Detector** is an NLP-based text classification project that analyzes written content and estimates whether it resembles **human-written or AI-generated text**.

Built using **DistilBERT**, the project fine-tunes a pretrained Transformer on paired human/AI Wikipedia content and turns the trained model into an interactive detection tool.

---

## 🚀 How It Works

```text
Wikipedia Human + AI Dataset
          ↓
Data Preparation & Labeling
          ↓
Human = 0 | AI = 1
          ↓
Train / Validation Split
          ↓
DistilBERT Tokenization
          ↓
Transformer Fine-Tuning
          ↓
Model Evaluation
          ↓
Saved AI Detection Model
          ↓
Streamlit Web App
          ↓
AI / Human Probability
```

The original dataset contains **9,970 human/AI text pairs**, which are transformed into approximately **19,940 labeled examples** for binary classification.

---

## 🧠 Tech Stack

| Technology            | Purpose                          |
| --------------------- | -------------------------------- |
| Python                | Core development                 |
| Hugging Face Datasets | Dataset loading & processing     |
| DistilBERT            | NLP classification model         |
| Transformers          | Tokenization & model fine-tuning |
| PyTorch               | Deep-learning inference          |
| Pandas                | Data preparation                 |
| NumPy                 | Numerical operations             |
| Scikit-learn          | Evaluation metrics               |
| Streamlit             | Interactive web interface        |

---

## ✨ Features

* 🧠 Transformer-based AI text classification
* 📊 AI & Human probability scores
* 🔍 Binary classification with an uncertainty range
* 📈 Accuracy, Precision, Recall & F1 evaluation
* 🧩 Confusion-matrix analysis
* ⚡ Lightweight DistilBERT architecture
* 🌐 Streamlit-based interactive interface

---

## 📁 Project Structure

```text
AI-Slop-Detector/
│
├── train_model.py
├── detector.py
├── app.py
│
└── ai_slop_model/
    ├── config.json
    ├── model.safetensors
    ├── tokenizer.json
    └── ...
```

---

## ▶️ Run Locally

Install dependencies:

```bash
pip install torch transformers datasets pandas numpy scikit-learn streamlit accelerate
```

Train the model:

```bash
python train_model.py
```

Test the detector:

```bash
python detector.py
```

Launch the web app:

```bash
streamlit run app.py
```

---

## 🎯 Why This Project?

Instead of relying on simple keyword matching or manually defined rules, this project uses **contextual language representations learned by a Transformer model** to distinguish between human-written and AI-generated examples.

It demonstrates a complete ML pipeline:

**Dataset → preprocessing → fine-tuning → evaluation → inference → deployment**

---

## ⚠️ Important Note

The detector produces a **probabilistic classification**, not definitive proof of AI authorship. Because the model is trained on Wikipedia human/AI text pairs, its performance may vary on text from other domains or AI systems.

---

### Built with Python 🐍 + Transformers 🤗 + PyTorch 🔥
