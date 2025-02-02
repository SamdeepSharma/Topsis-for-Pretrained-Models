# TOPSIS-Based Evaluation of Pretrained Models for Text Similarity

This project evaluates various **pretrained NLP models** for **text similarity** using **cosine similarity** and ranks them using the **TOPSIS** method. The goal is to identify the best model for sentence similarity tasks, ultimately providing a ranked list of models based on their effectiveness.

## 📌 Features

- Uses **multiple transformer-based models** (BERT, RoBERTa, SBERT, GPT-2, DistilBERT, DistilRoBERTa)
- Computes **cosine similarity** between two sentences using embeddings
- Applies **TOPSIS (Technique for Order of Preference by Similarity to Ideal Solution)** to rank models based on their similarity scores
- Outputs the results in a **CSV file** for easy comparison

## 🛠 Installation

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/SamdeepSharma/Topsis-for-Pretrained-Models
cd 'Topsis-for-Pretrained-Models'
```

### 2️⃣ Install Dependencies
```bash
pip install torch transformers scipy numpy matplotlib seaborn
```

## 🚀 Usage

Open the Python script in jupyter or google colab environment and run it.

## 📊 How It Works

1. **Pretrained models** are loaded from Hugging Face
2. **Cosine similarity** is calculated for the given sentence pairs using each model's embeddings
3. The **TOPSIS** method ranks the models based on their similarity scores, where the highest score gets rank 1
4. **Results** are saved in a CSV file named `model_topsis_rankings.csv`

## 📜 Example Sentences Used

```text
Sentence 1: "Despite the ostensibly positive impact of artificial intelligence on productivity, 
its unchecked proliferation raises profound ethical dilemmas, particularly in the domains of 
data privacy and algorithmic bias."

Sentence 2: "The paradox of technological progress lies in its dual potential: while fostering 
unprecedented efficiency, it simultaneously amplifies socio-economic disparities through 
automation-induced job displacement."
```

## 📁 Output (CSV File)

| Model | Rank | TOPSIS_Score | Similarity_Score |
|-------|------|--------------|------------------|
| GPT-2 | 1 | 1.000 | 0.996 |
| DistilRoBERTa | 2 | 0.971 | 0.991 |
| RoBERTa | 3 | 0.960 | 0.989 |
| DistilBERT | 4 | 0.332 | 0.872 |
| BERT | 5 | 0.055 | 0.820 |
| SBERT | 6 | 0.000 | 0.810 |

## 🖥 Models Used

* **BERT** (`bert-base-uncased`)
* **RoBERTa** (`roberta-base`)
* **Sentence-BERT (SBERT)** (`sentence-transformers/bert-base-nli-mean-tokens`)
* **GPT-2** (`gpt2`)
* **DistilBERT** (`distilbert-base-uncased`)
* **DistilRoBERTa** (`distilroberta-base`)

## 📌 Dependencies

* `torch` - For model inference
* `transformers` - For model loading and tokenization
* `scipy` - For cosine similarity computation
* `numpy` - For numerical operations
* `matplotlib`, `seaborn` - For plotting

## 🏆 Why Use This Project?

* ✅ Compare different **NLP models** for similarity tasks
* ✅ Get a **ranked list** of models based on TOPSIS scores for better selection
* ✅ **Fast and efficient** evaluation using pre-trained models for text embeddings