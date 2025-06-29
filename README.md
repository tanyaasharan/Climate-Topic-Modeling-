# Climate-Topic-Modeling-
This project applies topic modeling on climate-related corporate risk disclosures to extract meaningful themes and guide policy or risk analysis. Two vectorization strategies—CountVectorizer and TF-IDF—are compared using Latent Dirichlet Allocation (LDA) and coherence scoring.

## Project Overview 
The goal is to uncover latent themes within risk-labeled climate text data from corporate disclosures. Using LDA, we compare the effectiveness of CountVectorizer vs. TF-IDF-based topic modeling in terms of interpretability and coherence.

##  Data
* Source: Subset of climatebert/climate_sentiment (risk-labeled texts)
* Format: CSV with paragraph-level climate risk disclosures
* Preprocessing: tokenization, lowercasing, stopword removal

## Model Used

1. Latent Dirichlet Allocation (LDA)
- 5 topics modeled
- Gensim implementation
2. Topic extraction with:
- CountVectorizer
- TF-IDF Vectorizer

## Libraries Used

```
gensim
scikit-learn
nltk
pandas
numpy
matplotlib / seaborn
```
Install with:

```
pip install -r requirements.txt
```

## Methodology
1. Preprocess text using nltk and sklearn:
- Tokenize, remove stopwords, lemmatize
2. Convert documents to bag-of-words and TF-IDF matrices
3. Train LDA models on each representation
4. Evaluate topic quality using coherence scores
5. Visualize top keywords per topic

## Key Insights
* CountVectorizer preserved domain language better
* TF-IDF emphasized rare but potentially noisy words

##  Future Work
1. Use BERTopic or Top2Vec for contextualized embeddings
2. Test on “opportunity” or “neutral” texts for comparison
