## Sentiment Analysis

This section applies sentiment analysis to book descriptions to quantify the emotional tone of each book and explore its relationship with pricing.

---

### Objective
The goal of this analysis is to:
- Extract sentiment from book descriptions
- Convert unstructured text into numerical features
- Examine how sentiment varies across books and prices
- Prepare sentiment features for downstream analysis (dashboarding and machine learning)

---

### Data Sources
- **Cleaned book data**: Titles and prices obtained from prior web scraping and EDA
- **Book descriptions**: Scraped from the same source as the pricing data

The two datasets were merged on book title after standardizing column names.

---

### Methodology
- Sentiment analysis was performed using the **VADER (Valence Aware Dictionary and sEntiment Reasoner)** model
- For each book description, a **compound sentiment score** was calculated
- The compound score ranges from **-1 (very negative)** to **+1 (very positive)**
- Sentiment was categorized using standard thresholds:
  - Positive: score > 0.05
  - Neutral: -0.05 ≤ score ≤ 0.05
  - Negative: score < -0.05

---

### Features Created
- `sentiment_score`: Numeric compound sentiment score
- `sentiment_label`: Categorical sentiment classification (positive, neutral, negative)

These features enrich the original dataset and enable further analytical and predictive tasks.

---

### Output
The final dataset is saved as:

