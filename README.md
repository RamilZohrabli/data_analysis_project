# Event Data Analysis & Prediction – Baku  

GitHub Repository: [data_science_project](https://github.com/RamilZohrabli/data_science_project)  

---

## Project Overview  

This project focuses on collecting, cleaning, analyzing, and modeling event-related data from **[tickets-az.com](https://tickets-az.com)** for events in Baku.  

The workflow includes:  
1. **Data Collection** – Automated web scraping using the Google Custom Search API.  
2. **Data Preprocessing** – Cleaning, structuring, and enriching raw data.  
3. **Exploratory Data Analysis (EDA)** – Visualization and statistical insights.  
4. **Machine Learning Modeling** – Predicting event **price categories** based on event features.  

This project demonstrates the complete **data science pipeline**, from raw data acquisition to predictive modeling.  

---

## 1. Data Collection  

- Implemented **Google Custom Search API** to query event-related pages.  
- Extracted fields:  
  - Event Name  
  - Event Date  
  - Venue  
  - Price Range  
  - Event Details  
  - Region (Baku)  
  - Source URL  

📄 Output file: `scraped_data.csv`  

---

## 2. Data Preprocessing  

- Removed duplicates.  
- Normalized and imputed missing **dates**.  
- Extracted `Year`, `Month`, `Day`, `Weekday`.  
- Replaced missing venues with most frequent values.  
- Generated synthetic prices based on event type.  
- Structured clean dataset with the schema:  

| Event Name | Event Date | Year | Month | Day | Weekday | Event Type | Venue | Category | Price |  

📄 Final dataset: `processed_data.csv`  

---

## 3. Exploratory Data Analysis (EDA)  

Key visualizations:  
- Events by Year and Month  
- Price Distribution (Histogram + KDE)  
- Top Venues  
- Event Type vs Price (Boxplots)  
- Category vs Price  
- Event Frequency by Weekday  
- Correlation Heatmap  

(Visualizations available in Jupyter notebooks.)  

---

## 4. Machine Learning Model  

**Goal:** Classify events into **Low**, **Medium**, or **High** price categories.  

- **Feature Engineering**: Encoded categorical features + temporal features.  
- **Models Used**: Random Forest Classifier, XGBoost.  
- **Evaluation Metrics**: Accuracy, Precision, Recall, F1-Score, Confusion Matrix, ROC Curves, Feature Importance.  
- **Performance**: Achieved ~96% accuracy with strong generalization.  

---

## 5. Requirements  

Install dependencies:  

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost google-api-python-client
