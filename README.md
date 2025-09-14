# Data-Ingestion-System_ChatGPT-Google-Play-Reviews-Analysis

### 📋 Project Overview

This project implements a complete data pipeline for collecting, analyzing, and managing user review data for the official ChatGPT Android application on Google Play Store.

### 🎯 Objectives
Collect large-scale user review data from Google Play Store

Perform exploratory data analysis on review patterns and ratings

Establish an automated data ingestion pipeline to GitHub

Create a foundation for ongoing monitoring of user sentiment

### 🛠️ Technical Implementation
Data Collection
Tool Used: google-play-scraper Python package

Data Volume: 20,000 most recent user reviews

Parameters:

App ID: com.openai.chatgpt

Language: English (en)

Region: United States (us)

Sorting: Newest first

Data Analysis
Rating Distribution: Analysis of star rating patterns and skewness

Review Length: Examination of relationship between review length and ratings

Temporal Analysis: Review frequency and patterns over time

Metadata Validation: Verification of timestamp, user information, and rating completeness

Data Storage & Automation
Local Storage: CSV format (chatgpt_reviews.csv)

Cloud Backup: Automated pipeline to GitHub repository

Version Control: Integrated with Daisyzhao21/Data-Ingestion-System repository

Access Management: Configured GitHub Personal Access Token (PAT) for secure automation

### 📊 Key Findings
Rating Distribution
5-star ratings: 75.92% (15,184 reviews)

4-star ratings: 9.64% (1,928 reviews)

3-star ratings: 4.47% (894 reviews)

2-star ratings: 2.10% (419 reviews)

1-star ratings: 7.88% (1,575 reviews)

### Insights
Significant polarization in user sentiment (mostly 5-star or 1-star reviews)

Lower-rated reviews tend to be more detailed and explanatory

Consistent daily review volume indicates active user base

High-quality metadata enables robust analysis capabilities

### 🚀 Technical Achievements
End-to-End Pipeline: Established complete data flow from collection to storage

Automation Framework: Implemented GitHub API integration for automated updates

Analysis Foundation: Created comprehensive exploratory data analysis framework

Scalable Architecture: Designed system that can be extended to other applications

### 🔧 Installation & Usage
Prerequisites
bash
pip install google-play-scraper pandas matplotlib seaborn PyGithub
Basic Usage
python
from google_play_scraper import app, reviews, Sort

# Get app info
app_info = app('com.openai.chatgpt', lang='en', country='us')

# Scrape reviews
reviews_result, _ = reviews(
    'com.openai.chatgpt',
    lang='en',
    country='us',
    sort=Sort.NEWEST,
    count=1000
)
### 📈 Future Enhancements
Scheduled Collection: Implement regular automated data collection

Advanced Analytics: Incorporate sentiment analysis and topic modeling

Dashboard Development: Create interactive visualization dashboard

Multi-Platform Expansion: Extend to other app stores and platforms

Alert System: Implement notification system for rating changes or trends

### 📝 License
This project is open source and available under the MIT License.

#### 🤝 Contributing
Contributions, issues, and feature requests are welcome. Feel free to check issues page.

#### 📧 Contact
Daisyzhao21 - GitHub Profile

#### Project Link: https://github.com/Daisyzhao21/Data-Ingestion-System
