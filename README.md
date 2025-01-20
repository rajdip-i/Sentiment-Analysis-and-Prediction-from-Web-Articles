# Sentiment Analysis and Prediction from Web Articles

This project is centered on **Lexical Sentiment Analysis**, providing a comprehensive pipeline for automating sentiment detection in online articles. With the overwhelming volume of information available on the web, manually evaluating sentiments is both inefficient and impractical. This system extracts, cleans, and processes web content, leveraging lexical resources and Word2Vec embeddings to classify sentiments as positive, negative, or neutral. 

## Key Features
- **Article Extraction**: Automates article scraping from the web, supporting structured and unstructured content.
- **Lexical Sentiment Analysis**: Uses a predefined lexicon of positive and negative words to compute polarity scores, offering insights into the tone of the content.
- **Stopword Removal**: Implements custom stopword handling for cleaner and more meaningful text processing.
- **Polarity Scoring**: Calculates sentiment scores using tokenized text for fine-grained sentiment classification.
- **Word2Vec Integration**: Leverages pretrained Word2Vec models to generate document embeddings for semantic understanding.
- **Machine Learning**: Applies models such as Linear Regression, SVR, and XGBoost for sentiment prediction based on article embeddings.

## Directory Structure
```
.
├── README.md                        # Project documentation
├── Input.xlsx                       # Dataset with URLs for articles
├── Sentiment Analysis and Prediction from Web Articles_.ipynb # Jupyter notebook with the full pipeline
├── positive-words.txt               # List of positive sentiment words
├── negative-words.txt               # List of negative sentiment words
├── GoogleNews-vectors-negative300.bin # Pretrained Word2Vec model
```

## Workflow Overview
1. **Data Collection**: Extract articles from web URLs specified in an input Excel file.
2. **Text Cleaning**: Remove stopwords and filter words using the provided lexicon files.
3. **Sentiment Analysis**:
   - Compute sentiment polarity using the frequency of positive and negative words.
   - Generate a polarity score for each article.
4. **Embedding Creation**:
   - Use pretrained Word2Vec (`GoogleNews-vectors-negative300.bin`) to generate semantic embeddings for each document.
5. **Machine Learning Models**:
   - Train and evaluate regression models to predict sentiment scores.
   - Use metrics such as R2 Score, MAE, and RMSE to measure performance.

## Usage
1. Clone the repository.
2. Download the pretrained Word2Vec model (e.g., `GoogleNews-vectors-negative300.bin`) and place it in the project directory.
4. Run the Jupyter notebook `Sentiment Analysis and Prediction from Web Articles_.ipynb` to execute the pipeline.

## Dependencies
- Python Libraries: `pandas`, `nltk`, `scikit-learn`, `gensim`, `xgboost`, `beautifulsoup4`, and more.

