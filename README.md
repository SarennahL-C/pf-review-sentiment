# Amazon Product Reviews — Sentiment Analysis and Theme Identification

This capstone project applies **natural language processing (NLP)** techniques to analyse customer sentiment within Amazon product reviews. Using polarity-based sentiment classification and semantic similarity analysis, the project develops a scalable method for identifying **customer sentiment trends and recurring review themes** that can be shared with marketing and product management teams. The project combines quantitative sentiment scoring with qualitative insight extraction, demonstrating how large volumes of unstructured text data can be transformed into actionable business intelligence.

![alt text](customer-feedback.jpg)*Image sourced from Freepik.com*

---

### What’s in this repository

- **Jupyter Notebook:** full NLP analysis pipeline (`sentiment_analysis.ipynb`)  
- **Report:** written analysis and interpretation (`Sentiment analysis report.pdf`)  
- **Dataset:** Amazon product reviews (`Datafiniti_Amazon_Consumer_Reviews_of_Amazon_Products_May19.csv.zip`)  
- **Images:** visuals and feedback  
- **Requirements:** Python dependencies (`requirements.txt`)  

---

### Project Context

Understanding customer sentiment at scale is a core business problem for consumer-facing organisations. Manual review of thousands of customer comments is impractical, yet valuable insight is often embedded in free-text feedback.

This capstone project was designed to develop and test a **repeatable methodology** for:

- identifying positive, neutral, and negative sentiment in product reviews  
- analysing sentiment trends by brand and product category  
- identifying common themes within reviews using similarity-based clustering  

The approach was developed using a sample dataset `amazon review data short.csv` prior to potential application on larger production datasets.

---

### Dataset Overview

The dataset contains **28,332 Amazon and AmazonBasics product reviews**, of which:

- 27,071 reviews remained after duplicate removal  
- four key fields were retained:
  - product name  
  - brand  
  - product category  
  - review text  

The dataset includes reviews across multiple categories, with particularly large populations in **electronics** and **health & beauty** products.

---

### Approach Overview

The analysis was conducted in the following stages:

#### 1. Data Cleaning and Preparation
- Removal of duplicate rows  
- Selection and renaming of relevant fields  
- Verification of missing values  

#### 2. Sentiment Analysis
- Tokenisation and lemmatisation using spaCy  
- Removal of stop words to reduce noise  
- Polarity scoring using `spacytextblob`  
- Classification of reviews into:
  - positive  
  - neutral  
  - negative  

Sentiment boundaries were informed by **Net Promoter Score (NPS) methodology**, resulting in intentionally strict thresholds for positive sentiment.

#### 3. Sentiment Distribution Analysis
- Comparison of sentiment across brands (Amazon vs AmazonBasics)  
- Comparison across product categories  
- Identification of distribution width and polarity variance  

#### 4. Similarity and Theme Identification
- Semantic similarity computation between reviews  
- Agglomerative hierarchical clustering  
- Identification of representative reviews within each cluster  
- Interpretation of dominant themes within positive and negative reviews  

---

### Key Insights / Findings

- Polarity-based sentiment analysis enables consistent large-scale review classification, though with recognised linguistic limitations.  
- Token-level analysis can misinterpret comparative or contextual language, occasionally reversing intended sentiment.  
- AmazonBasics products showed a higher proportion of strongly positive reviews, likely reflecting different customer expectations for economy brands.  
- Electronics reviews exhibited sufficient population size for meaningful similarity analysis.  
- Cluster analysis revealed clear recurring themes within both positive and negative reviews, including:
  - tablet devices  
  - e-readers  
  - accessories and peripherals  
- Negative reviews tended to be significantly longer than positive reviews, suggesting potential correlation between review length and dissatisfaction.  

---

### Limitations

The analysis highlighted several known constraints of traditional NLP approaches:

- individual words are analysed independently rather than as contextual phrases  
- qualifiers and comparators (e.g. “less expensive”) may be misinterpreted  
- sarcasm, metaphor, and domain-specific knowledge are not captured  
- sentiment boundaries remain partly heuristic  

Despite these limitations, the methodology provides consistent, explainable results suitable for exploratory and operational use.

---

### Endorsement

Reviewer feedback highlighted the **strong quality and clarity of the submission**, with particular praise for:

- A **clear, well-structured report** that aligned closely with the task requirements  
- Thoughtful and well-justified **preprocessing decisions**, explained in appropriate detail  
- A **solid conceptual understanding of sentiment analysis**, including polarity interpretation and model limitations  
- Clean, well-organised writing that communicated analytical reasoning effectively  

Overall feedback noted that the project **meets and exceeds the requirements**, describing it as the type of work that would meaningfully strengthen a professional data science portfolio.

---

### Skills Demonstrated

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

### Requirements / How to Run

Install the required Python dependencies using `requirements.txt`.

---

### Why this project belongs in my portfolio
This capstone demonstrates my ability to apply NLP techniques to a realistic business problem involving unstructured text data. It combines technical implementation with critical interpretation, acknowledging both the power and limitations of sentiment analysis.

By integrating sentiment classification with similarity-based theme identification, the project shows how NLP outputs can be translated into insights meaningful to marketing, product management, and customer experience teams — a key requirement for real-world data science applications.
