# Team 26 - Data & Information Engineering Fall 2024 - Team Project

## Team Members

| Team 26                       | Contribution (%) |
|-------------------------------|------------------|
| Ramil Zohrabli (Team Leader)  | 25               |
| Ayhan Niyazli                 | 25               |
| Raul Aghayev                  | 25               |
| Halima Khanmammadova          | 25               |

 ### Github Repository URL: https://github.com/ADA-SITE-ENCE-3503/team-project-team-26.git
 
## Project Overview

The objective of this project is to collect, clean, analyze, and model event-related data from the website `tickets-az.com` using Python. The project involves web scraping, data processing, exploratory data analysis (EDA), and machine learning modeling.

### Project Topic: 
Event Data of Baku (e.g., type, dates, tickets, prices, etc.)

## Table of Contents

1. [Data Collection](#data-collection)
2. [Data Preprocessing](#data-preprocessing)
3. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
4. [Machine Learning Model](#machine-learning-model)
5. [Requirements](#requirements)
---

## Data Collection

### Objective

In this part of the project, we implemented a web scraper to collect event-related data from `tickets-az.com`. The web scraper retrieves data on events occurring in Baku, including event names, venues, prices, and dates, among other attributes.

### Key Steps

- **Web Scraping**: 
  We used the Google Custom Search API to collect data from `tickets-az.com`. The search query targets event-related pages and collects metadata such as event title, link, snippet, and display link.
  
- **Data Enrichment**: 
  The collected data was enriched with additional information such as:
  - Event Type
  - Event Date
  - Venue
  - Price Range
  - Keywords
  - Region (Baku)
  - Source URL

### Data Structure
The data is collected into a pandas DataFrame and saved into a `.csv` file with the following columns:
- Event Name
- Link
- Event Date
- Venue
- Price
- Event Details
- Keywords
- Region
- Event Type
- Source

---

## Data Preprocessing

### Key Steps

- **Handling Missing Values**: 
  Missing values were filled through appropriate imputation techniques such as:
  - Filling missing dates with random dates within a specific range.
  - Filling missing venue names with the most frequent venue name.
  
- **Column Modifications**: 
  - The 'Price Range' column was replaced with random price values between 40 and 250.
  - The 'Event Name' and 'Event Date' columns were rearranged to give a clearer dataset structure.
  
- **Duplicate Removal**: 
  Duplicate rows were removed to ensure data quality.

- **Data Saving**: 
  After preprocessing, the data was saved into a cleaned dataset `processed_data_team_26.csv`.

---

## Exploratory Data Analysis (EDA)

### Key Steps

- **Summary Statistics**: 
  Summary statistics were generated for the columns, helping to understand the overall distribution of data (e.g., prices, event dates).

- **Visualizations**:
  - Event distribution by year
  - Price distribution (Histogram & Kernel Density Estimation)
  - Top venues hosting the most events
  - Event prices by year (boxplot)
  
- **Correlations**:
  A correlation heatmap was generated for numeric columns to understand the relationships between features.

---

## Machine Learning Model

### Objective

In this part of the project, we applied machine learning techniques to predict the `Price Category` of events (Low, Medium, High) based on features such as venue, event day, and event year.

### Key Steps

- **Feature Engineering**:
  - Encoded categorical variables such as venue.
  - Created additional features such as day of the week, month, and year from the event date.
  
- **Model**:
  - We used the RandomForestClassifier from `sklearn` to train the model.
  - Cross-validation and accuracy evaluation were performed to assess the model's performance.

- **Result**: 
  The model evaluated classification metrics (accuracy, precision, recall, F1-score) and displayed a confusion matrix and feature importance.

---

## Requirements

The following libraries are required to run the project:

- `pandas` for data handling
- `googleapiclient` for web scraping
- `matplotlib`, `seaborn` for visualizations
- `scikit-learn` for machine learning tasks
- `numpy` for numerical operations


