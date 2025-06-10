# SentimentAnalysisUSElection2020

# Twitter Sentiment Analysis: Trump vs Biden (2020 U.S. Election)

A simple Python project that uses VADER sentiment analysis to compare the public’s Twitter sentiment toward Donald Trump and Joe Biden during the 2020 U.S. presidential election. We extract tweets containing campaign‐related hashtags, compute positive/neutral/negative counts, and visualize the results.

---

## 📁 Repository Structure

    .
    
    │--- hashtag_donaldtrump.csv       # Raw tweets for Trump
    │--- hashtag_joebiden.csv          # Raw tweets for Biden
    ├── sentiment_analysis_uselection.py  # Main analysis script/notebook
    ├── Results.png                       # Bar chart of sentiment counts
    └── README.md                         # This document

---

## 🛠 Dependencies

- Python 3.7+
- [vaderSentiment](https://pypi.org/project/vaderSentiment/)  
- requests  
- pandas  
- matplotlib  

Install via pip:

```bash
pip install vaderSentiment requests pandas matplotlib
```
## 🚀 Usage
Prepare your data
Place your two CSV files (hashtag_donaldtrump.csv and hashtag_joebiden.csv)

Run the analysis

```bash
python sentiment_analysis_uselection.py
```
This will:

- Load tweets for each candidate

- Compute VADER polarity scores and classify each tweet as Positive, Neutral, or Negative

- Aggregate counts by sentiment category

- Print summary statistics to the console

- Save a bar chart (Results.png) comparing sentiment counts side by side
---
## View the chart

📊 Results
| Candidate | Positive | Neutral | Negative |
|-----------|----------|---------|----------|
| Trump     | 31,631   | 31,256  | 37,112   |
| Biden     | 34,357   | 35,759  | 29,883   |


<img src="https://github.com/asoma0710/SentimentAnalysisUSElection2020/blob/main/Results.png" alt="Results" width="600"/>



## 🗳 Comparison with 2020 Election Outcome
Actual Result

- Joe Biden won the 2020 U.S. presidential election with 306 electoral votes (51.3% popular vote)

- Donald Trump received 232 electoral votes (46.8% popular vote)

- Sentiment vs. Votes

- Positive sentiment was slightly higher for Biden (34.4 k) than Trump (31.6 k).

- Negative sentiment was significantly higher for Trump (37.1 k) than Biden (29.9 k).

- Neutral sentiment counts were roughly comparable.

## Findings:

- Higher negative sentiment toward Trump aligns loosely with his lower popular‐vote share.

- More positive buzz around Biden may reflect the broader public’s lean in key swing states.

- However, Twitter sentiment is not a perfect proxy for voter behavior. Factors such as bot activity, hashtag campaigns, and demographic skews on social media can distort the picture.

## ⚠️ Caveats & Future Work
Sampling bias: Only tweets with specific hashtags were used.

Bot/spam filtering: No bot detection applied—automated accounts may skew results.

Time window: Analysis covers a particular period; public opinion shifted over many months.

Language & sarcasm: VADER may misclassify tweets with irony or mixed sentiment.

## Next steps:

Filter out retweets, non-English tweets, and likely bots.

Expand to multiple time windows (e.g., debates, Election Day).

Compare with actual polling data over time.
