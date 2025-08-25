# 🧠 Word Embeddings (Word2Vec & GloVe)

## What Are Word Embeddings?
Word embeddings are numerical representations of words that capture their **meaning** and **context**. Unlike TF-IDF or Bag of Words, which just count word frequency, embeddings place words in a high-dimensional space where similar words are **closer together**.

Example:
- "King" → [0.55, 0.78, 0.30, ...]
- "Queen" → [0.57, 0.80, 0.31, ...]

This allows us to do cool math like:
```
King - Man + Woman ≈ Queen
```

---

## Why Use Word Embeddings?
✅ Captures context and meaning  
✅ Dense vectors (not sparse like TF-IDF)  
✅ Forms the base for GPT, BERT, etc.  
✅ Words with similar usage get similar vectors  

---

## Word2Vec Overview

Word2Vec is a model that learns embeddings by predicting context.

### Two Architectures:
- **CBOW (Continuous Bag of Words):** Predicts a word from surrounding context.
- **Skip-Gram:** Predicts context from a target word (better for rare words).

### Training:
1. Starts with random vectors
2. Adjusts them during training using a shallow neural network
3. After training, words that appear in similar contexts end up with similar vectors

---

## Visualising Word Embeddings
We can use PCA or TSNE to reduce the high-dimensional vectors into 2D to **plot similar words together**.

Example:
Words like `money, loan, finance, bank` cluster together.

---

## GloVe (Global Vectors for Word Representation)
- Uses global word co-occurrence matrix
- Learns embeddings from word-pair statistics (instead of window-based prediction)
- Often pretrained on massive corpora like Wikipedia

---

## Tools Used:
- `gensim` – for training Word2Vec
- `nltk` – for corpus (Brown corpus)
- `matplotlib + sklearn` – for visualising vectors

---

## Realisation 💡
TF-IDF helped with frequency, but Word2Vec **understands relationships**. Now I can tell that “angry” and “furious” are similar, even if they’re not used together.

---

## Next:
🔜 BERT-style contextual embeddings (pretrained models like spaCy, Hugging Face)