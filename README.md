# bert-sentiment-analysis

# 🧠 Sentiment Analysis on Tweets Using BERT

## 📌 Overview
This project analyzes a sample set of noisy tweets and classifies their sentiment using a state-of-the-art transformer model. The workflow involves:
- Text cleaning and preprocessing
- Sentiment classification using **BERT (Twitter RoBERTa)**
- Extraction of sentiment **confidence scores**
- Visual exploration of results

## ⚙️ Tools & Libraries
- Python
- `pandas`, `re`, `matplotlib`, `seaborn`
- `transformers` by Hugging Face
- Pretrained model: `cardiffnlp/twitter-roberta-base-sentiment`

## 🧼 Data Preparation
The tweet dataset was manually created to include common noise:
- Mentions (`@username`)
- Hashtags
- Emojis
- URLs
- Slang and informal tone

A cleaning function was applied to:
- Remove special characters and links
- Normalize casing
- Strip unnecessary punctuation

## 🧠 Sentiment Analysis Approach
Used a BERT-based pipeline fine-tuned for social media text. For each tweet:
- A sentiment label was assigned: **Positive**, **Neutral**, or **Negative**
- A confidence score (from 0 to 1) was recorded, representing the model's certainty

## 📊 Results Snapshot

| Cleaned Tweet | Sentiment | Confidence |
|---------------|-----------|------------|
| openai is okay idk what the hype is about tbh | Neutral | 0.72 |
| LOVING what OpenAI is doing lately | Positive | 0.98 |
| OpenAI disappoints me sometimes | Negative | 0.89 |

## 📈 Key Insights
- BERT accurately identified **strong emotional language** (e.g., "LOVING", "disappoints") and assigned high confidence.
- Ambiguous or sarcastic tweets had **lower confidence scores**.
- Compared to `TextBlob`, BERT handled **context and slang more effectively**.

## 🔚 Conclusion
This prototype shows that transformer models like BERT offer powerful capabilities for nuanced sentiment classification, especially in noisy, informal text environments like Twitter.
