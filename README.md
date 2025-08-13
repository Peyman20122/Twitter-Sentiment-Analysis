# Text Classification with Word2Vec & BERT

## 📌 Overview
In this project, we worked on a text classification task for a client who requested model accuracy between **86% and 95%**.  
We implemented and compared two main models:

1. **Word2Vec → CNN → LSTM → Fully Connected Layer**  
2. **BERT → CNN → LSTM → Fully Connected Layer**

---

## ⚙ Models & Results

### **1. Word2Vec Model**
- **Pre-trained embeddings**: Used `cc.id.300.vec` from Facebook FastText.  
  This file contains **Indonesian word vectors** with 300 dimensions, trained on Common Crawl data.  
- **Pipeline**:  
  1. Word2Vec Embedding Layer (pre-trained vectors)  
  2. Convolutional Neural Network (CNN) for local feature extraction  
  3. LSTM for sequential pattern learning  
  4. Fully Connected Layer for classification  
- **Accuracy**: ~ **87%**

---

### **2. BERT Model**
- **Base model**: Pre-trained **BERT** from Google (Bidirectional Encoder Representations from Transformers).  
- **Why BERT?**
  - Unlike Word2Vec, which gives a fixed vector for each word, BERT understands **context**.  
    For example, the word *bank* in "river bank" vs. "money bank" has different meanings for BERT.  
  - Reads sentences **both left-to-right and right-to-left** (bidirectional), leading to better semantic understanding.  
  - Pre-trained on massive text datasets, so it performs well even with smaller training data.
- **Pipeline**:  
  1. BERT Embeddings  
  2. CNN for local pattern extraction  
  3. LSTM for sequential context learning  
  4. Fully Connected Layer for classification  
- **Accuracy**: ~ **90%**

---

## 📊 Comparison

| Model | Accuracy | Key Advantage |
|-------|----------|---------------|
| Word2Vec + CNN + LSTM | 87% | Faster, simpler, uses pre-trained vectors (`cc.id.300.vec`) |
| BERT + CNN + LSTM | 90% | Understands context, better for polysemy & complex sentences |

---

## 📂 Files
- `cc.id.300.vec` → Pre-trained Indonesian FastText word vectors (300 dimensions).  
- `Word2Vec+CNN+LSTM.ipynb` → Implementation of the Word2Vec model.  
- `BERT+CNN+LSTM.ipynb` → Implementation of the BERT model.  

---

## 🚀 Conclusion
We found that **BERT** consistently outperforms Word2Vec for this classification task, thanks to its contextual understanding of words and bidirectional architecture. However, Word2Vec still provides decent results with less computational cost.

---

## 🏷 Hashtags
`#NLP #BERT #Word2Vec #FastText #DeepLearning #TextClassification #SentimentAnalysis #CNN #LSTM #Keras`
