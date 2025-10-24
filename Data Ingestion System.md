# ChatGPT Google Play Reviews Analysis

## 📋 Project Overview

A comprehensive data pipeline for collecting, analyzing, and managing user reviews of the ChatGPT Android app from Google Play Store. The system handles everything from data ingestion to automated storage and insightful analysis.

## 🎯 Key Objectives

- **Collect** 20,000 user reviews from Google Play Store
- **Analyze** rating patterns, user sentiment, and version performance  
- **Automate** data pipeline with GitHub integration
- **Establish** foundation for continuous monitoring

## 🛠️ Technical Implementation

### Data Pipeline
- **Collection**: `google-play-scraper` package (20K reviews, English, US region)
- **Cleaning**: Removed 3 unnecessary columns (userImage, replyContent, repliedAt), handled missing values in version columns (7.25% filled with 'unknown')
- **Storage**: SQLite3 database with optimized schema and indexes
- **Analysis**: Rating distribution, version performance, temporal patterns

### Database Architecture
**SQLite3 Database**: `chatgpt_reviews.db`
- **Table**: `reviews` with 8 core columns including reviewId, userName, content, score, thumbsUpCount, reviewCreatedVersion, at, appVersion
- **Performance**: Indexed on score, appVersion, and thumbsUpCount for fast querying
- **Integrity**: Primary key constraints and data type validation
- **Management**: Automated backup system and size monitoring

### Core Features
- Automated data ingestion and validation
- Version performance tracking across 54 app versions
- Temporal analysis and user behavior insights
- Secure GitHub integration with PAT authentication
- Efficient SQL querying for complex analysis

## 📊 Key Insights

### Rating Distribution
- **75.8% Positive** (5 stars) - 15,163 reviews
- **9.6% Positive** (4 stars) - 1,926 reviews
- **4.5% Neutral** (3 stars) - 895 reviews
- **2.1% Negative** (2 stars) - 429 reviews
- **7.9% Negative** (1 star) - 1,587 reviews

### Overall Performance Metrics
- **Average Rating**: 4.43/5.00
- **Standard Deviation**: 1.19
- **Positive Reviews** (4-5 stars): 85.4%
- **Negative Reviews** (1-2 stars): 10.1%
- **NPS-like Score**: +65.7%

### Version Performance
**Total Versions Analyzed**: 54
- **Reliable Versions** (≥5 reviews): 24 (44.4%)
- **Small Sample Versions** (<5 reviews): 30 (55.6%)

**Top 3 Versions** (min. 5 reviews):
1. 1.2025.161 → 4.82 ⭐ (11 reviews)
2. 1.2025.084 → 4.80 ⭐ (10 reviews) 
3. 1.2025.147 → 4.62 ⭐ (13 reviews)

**Most Reviewed Version**: 1.2025.245 (12,069 reviews, 4.34 score)

### User Behavior Patterns
- **Review Polarization**: Strong tendency toward 5-star or 1-star ratings
- **Detailed Feedback**: Negative reviews tend to be longer and more explanatory
- **Global Reach**: Multi-lingual user base with diverse feedback
- **Temporal Pattern**: Highest average ratings at 20:00 (4.51)

### Version Evolution
- **Trend**: Slight improvement over time (slope: 0.0047)
- **Correlation**: No significant correlation between sample size and rating (0.118)
- **Consistency**: Ratings are relatively stable across versions

## 🚀 Quick Start

### Installation & Setup
Install required packages and run the database setup script. The system automatically creates the SQLite3 database with optimized schema and imports your review data.

### Database Features
- **Fast Querying**: Pre-built indexes enable rapid analysis
- **Data Integrity**: Constraint validation ensures clean data
- **Easy Backup**: Automated timestamped backups
- **Flexible Analysis**: Support for complex SQL queries

## 📈 Future Roadmap

- **Extended Analysis**: Longer time periods for trend identification
- **Advanced Analytics**: Sentiment analysis and topic modeling
- **Interactive Dashboard**: Real-time visualization platform
- **Multi-Platform**: Expand to iOS App Store and other regions

## 🔗 Resources

- **GitHub**: [Data Ingestion System](https://github.com/Daisyzhao21/Data-Ingestion-System)
- **Maintainer**: Daisyzhao21
- **License**: MIT

*Data Source: Google Play Store ChatGPT Reviews | Last Updated: September 2025*  
*Database: SQLite3 with 20,000+ optimized records*
