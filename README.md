# Sentiment Analysis Project with NLTK and Transformers

A comprehensive sentiment analysis project that leverages both traditional NLP techniques with NLTK and modern transformer-based models to classify the sentiment of Amazon food reviews.

## Features

- **Sentiment Classification**: Binary classification of reviews into positive and negative sentiments
- **Multiple Approaches**:
  - NLTK-based sentiment analysis using lexicon-based methods
  - Transformer-based models for state-of-the-art performance
- **Dataset**: Amazon Fine Food Reviews dataset with 568,454 reviews
- **Interactive Notebook**: Jupyter notebook for exploratory data analysis and model building
- **Preprocessing Pipeline**: Text cleaning, tokenization, and normalization

## Project Structure

```
.
├── README.md                    # Project documentation
├── main.ipynb                   # Main Jupyter notebook with analysis and models
├── .gitignore                   # Git ignore configuration
└── datasets/
    └── snap/
        └── amazon-fine-food-reviews/
            └── versions/2/
                └── Reviews.csv  # Amazon Fine Food Reviews dataset
```

## Dataset

- **Source**: [Amazon Fine Food Reviews - Kaggle](https://www.kaggle.com/snap/amazon-fine-food-reviews)
- **Records**: 568,454 reviews
- **Features**: Review ID, Product ID, User ID, Profile Name, Helpful votes, Review Text, Rating, Time

The dataset includes reviews with ratings from 1 to 5 stars, which can be used for both binary (positive/negative) and multi-class sentiment classification.

## Installation

### Prerequisites

- Python 3.11+
- pip or conda package manager

### Setup

1. **Clone the repository**:

   ```bash
   git clone https://github.com/fksifat/Sentiment-Analysis-Project-with-NLTK-and-Transformers.git
   cd "Sentiment Analysis Project with NLTK and Transformers"
   ```

2. **Create a virtual environment**:

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

### Required Libraries

- **nltk**: Natural Language Toolkit for traditional NLP
- **pandas**: Data manipulation and analysis
- **numpy**: Numerical computing
- **scikit-learn**: Machine learning algorithms
- **transformers**: Hugging Face transformers for deep learning models
- **torch**: PyTorch deep learning framework
- **jupyter**: Interactive notebook environment
- **matplotlib**: Data visualization
- **seaborn**: Statistical data visualization

## Usage

### Running the Notebook

1. **Start Jupyter**:

   ```bash
   jupyter notebook
   ```

2. **Open `main.ipynb`** in your browser

3. **Execute cells sequentially** to:
   - Load and explore the dataset
   - Preprocess review text
   - Build and train sentiment models
   - Evaluate model performance
   - Make predictions on new reviews

### Quick Start Example

```python
# Example usage for sentiment prediction
from transformers import pipeline

sentiment_pipeline = pipeline("sentiment-analysis", model="distilbert-base-uncased-finetuned-sst-2-english")
result = sentiment_pipeline("This product is amazing!")
print(result)  # Output: [{'label': 'POSITIVE', 'score': 0.99}]
```

## Models & Approaches

### NLTK Approach

- Lexicon-based sentiment analysis
- VADER sentiment analyzer
- Simple and interpretable results
- Fast inference

### Transformer-Based Models

- DistilBERT: Lightweight version of BERT
- BERT: State-of-the-art contextual embeddings
- RoBERTa: Robustly Optimized BERT
- Fine-tuning on custom datasets for improved performance

## Results & Metrics

The notebook includes:

- **Accuracy**: Overall correctness of predictions
- **Precision & Recall**: For positive and negative classes
- **F1-Score**: Harmonic mean of precision and recall
- **Confusion Matrix**: Visualization of classification results
- **ROC Curves**: Performance comparison across models

## Data Preprocessing

The pipeline includes:

1. **Text Cleaning**: Removal of HTML tags, special characters, and URLs
2. **Lowercasing**: Standardization of text
3. **Tokenization**: Breaking text into individual words/tokens
4. **Stop Word Removal**: Filtering common words (optional)
5. **Lemmatization**: Reducing words to base forms

## Contributing

Contributions are welcome! Please feel free to:

- Fork the repository
- Create a feature branch
- Submit pull requests with improvements

## License

This project is open source and available under the MIT License.

## Author

**Farhan Kabir Sifat**

- GitHub: [@fksifat](https://github.com/fksifat)
- Email: farhan017kabir@gmail.com

## Acknowledgments

- Amazon Fine Food Reviews dataset from SNAP (Stanford Network Analysis Project)
- NLTK and Hugging Face Transformers communities
- Open source contributors

## References

- [NLTK Documentation](https://www.nltk.org/)
- [Hugging Face Transformers](https://huggingface.co/transformers/)
- [Natural Language Processing Guide](https://www.youtube.com/watch?v=oM-Zw-SyKdA)
- [Sentiment Analysis Techniques](https://en.wikipedia.org/wiki/Sentiment_analysis)

---

**Last Updated**: March 2026
