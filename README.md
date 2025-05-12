# sentiment-analysis-for-social-media
pip install nltk
import nltk
nltk.download('vader_lexicon')
from nltk.sentiment.vader import SentimentIntensityAnalyzer

# Initialize the analyzer
sid = SentimentIntensityAnalyzer()

# Sample social media texts
texts = [
    "I love this product! It's amazing!",
    "This is the worst experience I've ever had.",
    "Meh, it was okay. Not great, not terrible.",
    "Totally blown away by the support team!"
]

# Analyze each text
for text in texts:
    scores = sid.polarity_scores(text)
    print(f"Text: {text}")
    print(f"Scores: {scores}\n")
