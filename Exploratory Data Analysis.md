# ChatGPT Mobile App Reviews - Exploratory Data Analysis


## 📁 Dataset Information
Original Dataset<br>
Records: 20,000 reviews<br>
Features: 11 columns<br>
Time Range: September 9-13, 2025<br>
Memory Usage: 1.7+ MB<br>

Processed Dataset<br>
Records: 20,000 reviews<br>
Features: 8 columns (after cleaning)<br>
Memory Usage: 1.2+ MB<br>


## 🧹 Data Preprocessing

### Columns Removed
userImage: User avatar URLs (no analytical value)<br>
replyContent: 0 non-null values (completely missing)<br>
repliedAt: 0 non-null values (completely missing)<br>

### Columns Retained
reviewId: Unique identifier for each review<br>
userName: User identification (kept for basic user behavior analysis)<br>
content: Review text (primary field for sentiment analysis)<br>
score: User rating (1-5 stars, key metric for satisfaction analysis)<br>
thumbsUpCount: Number of likes (usefulness indicator)<br>
reviewCreatedVersion: App version when review was created<br>
at: Review timestamp (converted to datetime)<br>
appVersion: App version information<br>

### Missing Value Treatment
reviewCreatedVersion & appVersion: Filled 1,450 missing values (7.25%) with "unknown"

## 🔍 Key Findings
Score	Count	Percentage<br>
5 ⭐	15,163	75.8%<br>
4 ⭐	1,926	9.6%<br>
3 ⭐	895	4.5%<br>
2 ⭐	429	2.1%<br>
1 ⭐	1,587	7.9%<br>

Overall Statistics:
Average Rating: 4.43/5.00<br>
Standard Deviation: 1.19<br>
Positive Reviews (4-5 stars): 85.4%<br>
Negative Reviews (1-2 stars): 10.1%<br>
NPS-like Score: +65.7%<br>

Version Performance Analysis
Version Data Quality<br>
Total Versions: 54<br>

Reliable Versions (≥5 reviews): 24 (44.4%)<br>
Small Sample Versions (<5 reviews): 30 (55.6%)<br>
Top Performing Versions (Minimum 5 Reviews)<br>
1.2025.161: 4.82 (11 reviews)<br>
1.2025.084: 4.80 (10 reviews)<br>
1.2025.147: 4.62 (13 reviews)<br>
1.2025.210: 4.60 (133 reviews)<br>
1.2025.217: 4.54 (293 reviews)<br>



Key Insights:

Most reviewed version: 1.2025.245 (12,069 reviews, 4.34 score)<br>
No significant correlation between sample size and rating (correlation: 0.118)<br>
Version evolution shows slight improvement trend (slope: 0.0047)<br>

Temporal Patterns
Data Collection Period: Only 5 days (Sep 9-13, 2025)<br>
Hourly Pattern: Highest ratings at 20:00 (4.51 average)<br>
Limitation: Insufficient data for monthly/quarterly/annual trend analysis<br>

Review Content Analysis
Content Length: Negative reviews tend to be longer (users provide detailed explanations)<br>
Language Diversity: Multiple languages present in reviews<br>
Usefulness: Low correlation between score and thumbs-up count<br>


## 📈 Business Insights
Strengths
High User Satisfaction: 85.4% positive ratings indicate excellent product-market fit<br>
Version Stability: Consistent performance across different versions<br>
User Engagement: Diverse user base with meaningful feedback<br>

Areas for Attention
Class Imbalance: Severe skew toward positive reviews may challenge sentiment analysis models<br>
Limited Time Range: 5-day data window restricts trend analysis<br>
Version Sample Sizes: 55.6% of versions have insufficient reviews for reliable analysis<br>


🛠 Technical Recommendations
Data Collection Improvements<br>
Extend data collection period for meaningful trend analysis<br>
Implement consistent version tracking<br>
Consider stratified sampling for balanced datasets<br>
