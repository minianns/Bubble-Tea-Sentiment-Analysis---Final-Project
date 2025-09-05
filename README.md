# Bubble-Tea-Sentiment-Analysis-Final-Project

## 1. Project Title
🧋 Bubble Tea Sentiment Analysis (International Reviews of Bubble Tea)

## 2. Problem Statement or Research Question
</br>
❓ Research Questions :</br>
1. Can refined NLP feature engineering and model tuning improve sentiment classification accuracy and yield actionable business insights?</br>
2. How to build an automated model to classify review sentiment (positive/neutral/negative) for bubble tea across brands and regions?</br>
3. Which factors (sweetness, texture, price, wait time, service) most influence customer opinions?</br></br>

## 3. Description of the Project
📝 Project Description</br>
Leverage large-scale dining review data to extract “bubble tea / milk tea” related texts, train a sentiment classifier, and generate business insights from keywords, topics, and geo/brand comparisons (e.g., popular flavors, frequent complaints, city/brand differences, seasonality).

💡 (With a BA foundation and hands-on marketing experience, I focus on turning customer feedback into actionable business decisions. I chose “Bubble Tea Sentiment Analysis” because the domain is concrete and brand-oriented, allowing unstructured text to be transformed into measurable KPIs (e.g., sentiment distribution, top keywords, geographic differences) that inform marketing and operations. The workflow is highly transferable: the same NLP + classification pipeline applies to e-commerce product reviews, restaurant delivery platforms, and travel ratings, enabling a repeatable and extensible analytics framework and dashboard outputs.)</br>

## 4. Data Sources
📂 Data Sources</br>
1. Primary (recommended): Yelp Open Dataset (JSON)</br>
* Download business.json and review.json.</br>
* Filter business.json by categories for “Bubble Tea” (optionally include “Coffee & Tea”, “Tea Rooms”).</br>
* Join review.json via business_id to obtain all related reviews (scales to thousands+ quickly).</br>
* Use star ratings for weak labels (≥4 = positive, 3 = neutral, ≤2 = negative), then manually validate a small sample.</br>

2. Secondary (compliant add-	on): Yelp Fusion API</br>
* Query “bubble tea / boba / pearl milk tea” across multiple cities (e.g., Vancouver, Toronto, SF, LA, NYC, Singapore, Taipei) and fetch a small number of reviews per business; aggregate across cities.</br>

3. Auxiliary (volume proxy): Google Trends via pytrends</br>
* Fetch regional/time-series interest for “bubble tea / boba” to compare with sentiment trends.</br>

4. Ethics & Compliance</br>
* Use official open datasets and APIs only; avoid scraping restricted platforms.</br>
* Keep only essential fields (text, rating, time, location), avoid PII.</br>
* Provide clear data usage notes (Data Card) and a Model Card.</br>


## 5. Tools & Technologies
🛠 Tools & Technologies</br>
1. Python: pandas, numpy, scikit-learn, matplotlib (and/or seaborn)</br>
2. NLP: TfidfVectorizer (scikit-learn), spaCy / NLTK; (advanced) transformers (DistilBERT)</br>
3. Models: Logistic Regression, Linear SVM, Naive Bayes, XGBoost (compare 2–3)</br>
4. Extras: pytrends (Google Trends), geopandas/folium (optional maps)</br>
5. Dev/Versioning: Jupyter Notebook, GitHub</br>


## 6. Planned Workflow / Methods
⚙️ Workflow / Methods</br>
1. Acquisition & Join: Yelp Open Dataset → filter bubble tea businesses → join reviews.</br>
2. Cleaning: deduplication, language detection (primarily EN; handle ZH/JP/KR if needed), emoji/punctuation handling.</br>
3. Labeling: weak labels from star ratings, small-scale manual validation.</br>
4. Feature Engineering: TF-IDF (1–2 grams), stopwords, lemmatization; (advanced) embeddings/transformers.</br>
5. Modeling (Baseline→Advanced):
Baseline: TF-IDF → Logistic Regression / Linear SVM / Naive Bayes
Advanced: XGBoost (with TF-IDF features); optional DistilBERT fine-tuning</br>
6. Evaluation & Tuning: stratified splits; Macro F1, Accuracy, confusion matrix; Grid/Random Search.</br>
7. Explainability & Insights: top positive/negative keywords, (optional) SHAP, brand/city × sentiment tables, time trends (overlay Google Trends).</br>
8. Visualization & Packaging: charts/maps, (optional) dashboard, final report & slides.


## 7. Expected Outcome or Deliverables
🎯 Expected Deliverables
1. Sentiment classifier (baseline + best) with evaluation (Macro F1, confusion matrix).</br>
2. Business insights: brand/city differences, top likes/dislikes, seasonal patterns.</br>
3. Technical artifacts: data processing scripts, feature/model notebooks, Model Card & Data Card.</br>
4. Presentation assets: 15 min slide deck; GitHub repo with README and figures.






