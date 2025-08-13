# Twitter-Sentiment-Analysis

# 📌 SnappFood Sentiment Analysis with BERT

This project builds a **sentiment analysis** model for SnappFood customer reviews.  
The goal is to classify reviews as **positive**, **negative**, or **neutral** to enable intelligent responses or managerial insights.

---

## ✨ Features

- Uses **ParsBERT** (Persian BERT) for high accuracy
- Supports three sentiment classes: `positive`, `negative`, `neutral`
- Persian text preprocessing (punctuation removal, normalization, tokenization)
- Retrainable with new datasets
- Ready for deployment as an API or Chatbot

---

## 📂 Project Structure

```
.
├── data/               # Datasets (raw and cleaned)
│   ├── raw.csv
│   ├── cleaned.csv
├── notebooks/          # Jupyter notebooks for experiments and analysis
│   ├── preprocessing.ipynb
│   ├── training.ipynb
├── src/                # Core project code
│   ├── preprocess.py   # Text cleaning functions
│   ├── train.py        # Model training code
│   ├── inference.py    # Sentiment prediction code
├── models/             # Saved models
├── requirements.txt    # Required dependencies
└── README.md           # This file
```

---

## 🔧 Installation

1. Clone the repository:

```bash
git clone https://github.com/username/snappfood-sentiment-bert.git
cd snappfood-sentiment-bert
```

2. Create a virtual environment and install dependencies:

```bash
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

---

## 📊 Training the Model

1. Place the dataset inside the `data/` folder.
2. Preprocess the data:

```bash
python src/preprocess.py
```

3. Train the model:

```bash
python src/train.py
```

The trained model will be saved inside the `models/` directory.

---

## 🚀 Sentiment Prediction

To predict the sentiment of a single review:

```bash
python src/inference.py "The food was delicious and hot"
# Output: positive
```

---

## 🧠 Model and Technologies

- **ParsBERT** from [HooshvareLab](https://github.com/hooshvare/parsbert)
- **Transformers** (HuggingFace)
- **PyTorch**
- **Hazm** for Persian NLP preprocessing

---

## 📌 Future Ideas

- Integrate with **ChatGPT API** for automated customer responses
- Build an **analytics dashboard** for managers
- Compress the model with DistilBERT or Quantization for faster inference

---

## 👨‍💻 Author

- Name: *Your Name*
- Email: you@example.com
- GitHub: [Your GitHub](https://github.com/username)
