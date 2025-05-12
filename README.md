 🛍️ Customer Purchase Pattern Analysis and Recommendation System

 📘 Project Overview

This project analyzes customer purchase data from an online retail store to understand shopping behavior and generate personalized product recommendations. It combines **rule-based**, **collaborative filtering**, **content-based filtering**, and **association rule mining** to improve customer engagement and drive sales.


🎯 Problem Statement

Retailers often struggle to identify what products to recommend to individual customers. This project addresses this by:

* Analyzing historical purchase data
* Identifying high-value customers
* Generating "buy again", "frequently bought together", and trending item recommendations
* Clustering users based on purchasing behavior using **RFM segmentation**


⚙️ Features & Approach

1. **Data Cleaning & Preprocessing**

   * Handled missing descriptions and invalid quantities
   * Parsed invoice dates, extracted time features

2. **Exploratory Data Analysis**

   * Visualized top-selling products by day, month, and country
   * Identified peak shopping hours and spending patterns

3. **Recommendation Systems**

   * **Rule-based**: Popular products, country-wise & time-wise top items
   * **Buy Again**: Recommends items the user previously bought
   * **Market Basket Analysis**: Using Apriori algorithm for bundle suggestions
   * **Collaborative Filtering**:

     * Customer-based using cosine similarity
     * Item-based using shared purchaser behavior
   * **Content-Based Filtering**:

     * Used TF-IDF, Word2Vec, GloVe, and FastText to find semantically similar items
     * Multiple similarity metrics: Cosine, Manhattan, Euclidean

4. **Customer Segmentation**

   * Used **RFM analysis** (Recency, Frequency, Monetary value)
   * Categorized customers into strategic segments for targeted marketing



🧰 Technologies Used

* **Python**: pandas, NumPy, matplotlib, seaborn
* **MLXTend**: Apriori & association rules
* **Scikit-learn**: Similarity metrics, KNN
* **Gensim**: Word2Vec, FastText
* **NLP**: TF-IDF, CountVectorizer
* **Matplotlib & Seaborn**: Data visualization



📊 Evaluation

* Recommendations are qualitatively evaluated based on:

  * Actual co-occurrence in invoices
  * Relevance of similar item descriptions
  * Diversity across models (TF-IDF vs Word2Vec vs FastText)
* No single metric used, but **cosine similarity and support-confidence-lift** in rules were key drivers

💡 Future Work

* Deploy recommendation engine as an interactive web app (Streamlit or Flask)
* Integrate user feedback loop for improving recommendations
* Handle cold-start problem using hybrid models
* Visual dashboard for business insights



