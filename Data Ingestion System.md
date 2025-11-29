# ChatGPT Google Play Reviews Analysis

## 📋 Project Overview

A comprehensive data pipeline for collecting, analyzing, and managing user reviews of the ChatGPT Android app from Google Play Store. The system handles everything from data ingestion to automated storage and insightful analysis with advanced sentiment analysis capabilities.

## 🎯 Key Objectives

- **Collect** 20,000+ reviews from Google Play Store
- **Analyze** rating patterns and user sentiment using TextBlob
- **Automate** data pipeline with continuous monitoring
- **Visualize** insights through comprehensive dashboards

## 🛠️ Technical Implementation

### Data Pipeline
- **Collection**: `google-play-scraper` package
- **Storage**: SQLite3 with optimized schema and indexes
- **Processing**: Automated cleaning and validation
- **Analysis**: Multi-method sentiment validation

### Sentiment Analysis
- **Primary Model**: TextBlob (NLTK-based lexicon approach)
- **Validation**: Score-based classification + consistency checks
- **Performance**: 75-85% agreement between methods
- **Speed**: 100-200 reviews/second processing

## 📊 Key Insights

### Rating Distribution
- **85.4% Positive** (4-5 stars) 
- **10.1% Negative** (1-2 stars)
- **4.5% Neutral** (3 stars)
- **Average Rating**: 4.43/5.00

### Version Performance
- **54 versions** analyzed
- **Top Version**: 1.2025.161 (4.82 ⭐)
- **Most Reviewed**: 1.2025.245 (12,069 reviews)
- **Stable Performance**: Consistent across versions

## 🚀 Quick Start

```bash
# Install dependencies
pip install -r requirements.txt

# Download NLTK data
python -c "import nltk; nltk.download('punkt'); nltk.download('brown')"

# Run pipeline
python main_automation.py
```

## 🔧 Core Features

- **Automated Data Collection** - Continuous review monitoring
- **Multi-Method Analysis** - TextBlob + score-based validation  
- **Performance Tracking** - Version comparison and trends
- **Efficient Storage** - SQLite3 with optimized queries

## 📈 Business Impact

- **User Insight** - Deep understanding of satisfaction drivers
- **Product Guidance** - Data-driven feature improvements  
- **Quality Monitoring** - Continuous performance tracking
- **Competitive Analysis** - Market comparison foundation

## 🔮 Future Enhancements

- **Advanced Models** - BERT/Transformer integration
- **Multi-Platform** - iOS App Store expansion
- **Real-time Dashboard** - Interactive visualization
- **Topic Modeling** - Automated insight generation

## 🔗 Resources

- **GitHub**: [Data Ingestion System](https://github.com/Daisyzhao21/Data-Ingestion-System)
- **Maintainer**: Daisyzhao21
- **License**: MIT
- **Data Source**: Google Play Store ChatGPT Reviews

---

*Comprehensive app review analysis combining traditional metrics with advanced sentiment analysis for actionable user insights.*
