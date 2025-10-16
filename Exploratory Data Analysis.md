# ChatGPT Mobile App Reviews - Exploratory Data Analysis


## 📁 Dataset Information
Original Dataset
Records: 20,000 reviews
Features: 11 columns
Time Range: September 9-13, 2025
Memory Usage: 1.7+ MB

Processed Dataset
Records: 20,000 reviews
Features: 8 columns (after cleaning)
Memory Usage: 1.2+ MB


## 🧹 Data Preprocessing

### Columns Removed
userImage: User avatar URLs (no analytical value)
replyContent: 0 non-null values (completely missing)
repliedAt: 0 non-null values (completely missing)

### Columns Retained
reviewId: Unique identifier for each review
userName: User identification (kept for basic user behavior analysis)
content: Review text (primary field for sentiment analysis)
score: User rating (1-5 stars, key metric for satisfaction analysis)
thumbsUpCount: Number of likes (usefulness indicator)
reviewCreatedVersion: App version when review was created
at: Review timestamp (converted to datetime)
appVersion: App version information

### Missing Value Treatment
reviewCreatedVersion & appVersion: Filled 1,450 missing values (7.25%) with "unknown"

## 🔍 Key Findings
Score	Count	Percentage
5 ⭐	15,163	75.8%
4 ⭐	1,926	9.6%
3 ⭐	895	4.5%
2 ⭐	429	2.1%
1 ⭐	1,587	7.9%

Overall Statistics:
Average Rating: 4.43/5.00
Standard Deviation: 1.19
Positive Reviews (4-5 stars): 85.4%
Negative Reviews (1-2 stars): 10.1%
NPS-like Score: +65.7%

Version Performance Analysis
Version Data Quality
Total Versions: 54

Reliable Versions (≥5 reviews): 24 (44.4%)
Small Sample Versions (<5 reviews): 30 (55.6%)
Top Performing Versions (Minimum 5 Reviews)
1.2025.161: 4.82 (11 reviews)
1.2025.084: 4.80 (10 reviews)
1.2025.147: 4.62 (13 reviews)
1.2025.210: 4.60 (133 reviews)
1.2025.217: 4.54 (293 reviews)



Key Insights:

Most reviewed version: 1.2025.245 (12,069 reviews, 4.34 score)
No significant correlation between sample size and rating (correlation: 0.118)
Version evolution shows slight improvement trend (slope: 0.0047)

Temporal Patterns
Data Collection Period: Only 5 days (Sep 9-13, 2025)
Hourly Pattern: Highest ratings at 20:00 (4.51 average)
Limitation: Insufficient data for monthly/quarterly/annual trend analysis

Review Content Analysis
Content Length: Negative reviews tend to be longer (users provide detailed explanations)
Language Diversity: Multiple languages present in reviews
Usefulness: Low correlation between score and thumbs-up count


## 📈 Business Insights
Strengths
High User Satisfaction: 85.4% positive ratings indicate excellent product-market fit
Version Stability: Consistent performance across different versions
User Engagement: Diverse user base with meaningful feedback

Areas for Attention
Class Imbalance: Severe skew toward positive reviews may challenge sentiment analysis models
Limited Time Range: 5-day data window restricts trend analysis
Version Sample Sizes: 55.6% of versions have insufficient reviews for reliable analysis


🛠 Technical Recommendations
Data Collection Improvements
Extend data collection period for meaningful trend analysis
Implement consistent version tracking
Consider stratified sampling for balanced datasets

Analytical Priorities
Text Sentiment Analysis: Leverage review content for deeper insights

Version Impact Assessment: Correlate specific features with user satisfaction

Negative Review Analysis: Focus on 10.1% critical feedback for product improvement

