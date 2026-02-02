# Amazon Product Reviews — Sentiment Analysis and Theme Identification

This capstone project applies **natural language processing (NLP)** techniques to analyse customer sentiment within Amazon product reviews. Using polarity-based sentiment classification and semantic similarity analysis, the project develops a repeatable methodology for identifying **sentiment trends and recurring review themes** that can be shared with marketing and product management teams.

The analysis combines quantitative sentiment scoring with qualitative theme extraction, demonstrating how large volumes of unstructured text data can be transformed into actionable business insight.

![Customer feedback illustration](customer-feedback.jpg)

<sub>Image sourced from Freepik.com.</sub>

---

## What’s in this repository

- **Jupyter Notebook:** full NLP analysis pipeline (`sentiment_analysis.ipynb`)  
- **Report:** written analysis and interpretation (`Sentiment analysis report.pdf`)  
- **Dataset:** Amazon product reviews (`Datafiniti_Amazon_Consumer_Reviews_of_Amazon_Products_May19.csv.zip`)  
- **Images:** visualisations and reviewer feedback  
- **Requirements:** Python dependencies (`requirements.txt`)  

---

## Project Context

Understanding customer sentiment at scale is a core business challenge for consumer-facing organisations. While individual reviews provide valuable feedback, manually analysing thousands of free-text comments is impractical.

This project was designed to develop a **scalable and interpretable NLP workflow** for:

- classifying customer sentiment as positive, neutral, or negative  
- analysing sentiment distribution across brands and product categories  
- identifying recurring themes within reviews using similarity-based clustering  

The approach was initially developed and validated on a reduced dataset before being applied to a larger review corpus.

---

## Approach Overview

The analysis followed a structured NLP workflow:

- Data cleaning, deduplication, and field selection  
- Text preprocessing using spaCy (tokenisation, lemmatisation, stop word removal)  
- Polarity-based sentiment scoring using `spacytextblob`  
- Classification of reviews into sentiment categories using strict thresholds informed by Net Promoter Score (NPS) methodology  
- Sentiment distribution analysis by brand and product category  
- Semantic similarity computation and hierarchical clustering  
- Identification and interpretation of dominant review themes using representative examples  

Throughout the analysis, emphasis was placed on transparency, reproducibility, and interpretability.

---

## Key Insights / Findings

- Polarity-based sentiment analysis enables consistent large-scale review classification, while retaining interpretability.  
- Token-level sentiment approaches can misinterpret comparative or contextual language, occasionally reversing intended meaning.  
- AmazonBasics products showed a higher proportion of strongly positive reviews, likely reflecting different customer expectations for economy brands.  
- Electronics reviews provided sufficient volume for meaningful similarity-based theme identification.  
- Cluster analysis revealed clear recurring themes within both positive and negative reviews, including:
  - tablet devices  
  - e-readers  
  - accessories and peripherals  
- Negative reviews tended to be significantly longer than positive reviews, suggesting a relationship between dissatisfaction and review length.  

---

## Endorsement

Reviewer feedback highlighted the **strong quality and clarity of the submission**, with particular praise for:

- A **clear, well-structured report** closely aligned with task requirements  
- Thoughtful and well-justified **preprocessing decisions**, explained in appropriate detail  
- A **solid conceptual understanding of sentiment analysis**, including polarity interpretation and known limitations  
- Clean, well-organised writing that communicated analytical reasoning effectively  

Overall feedback noted that the project **meets and exceeds the requirements**, describing it as work that would meaningfully strengthen a professional data science portfolio.

---

## Skills Demonstrated

**Analysis**
- Large-scale text preprocessing  
- Exploratory sentiment analysis  
- Distribution and variance interpretation  

**Modelling**
- NLP with spaCy and TextBlob  
- Polarity-based sentiment classification  
- Semantic similarity measurement  
- Hierarchical clustering  

**Evaluation**
- Interpretation of NLP limitations  
- Theme extraction using representative reviews  
- Translation of analytical outputs into business insight  

**Tools**
- Python  
- pandas  
- NumPy  
- spaCy  
- spacytextblob  
- SciPy  
- matplotlib / seaborn  
- Jupyter Notebook  

---

## Requirements

Install the required Python packages with: `pip install -r requirements.txt`

---

## Why this project belongs in my portfolio
This capstone demonstrates my ability to apply NLP techniques to a realistic business problem involving unstructured text data.

By combining sentiment classification with similarity-based theme identification, the project shows how NLP outputs can be translated into insights meaningful to marketing, product management, and customer experience teams. It also reflects a balanced approach that acknowledges both the power and limitations of sentiment analysis in real-world applications.
