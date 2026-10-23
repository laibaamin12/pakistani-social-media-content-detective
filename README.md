# Pakistani Social Media Content Detective

An end-to-end exploratory data analysis (EDA) of 3,000 simulated social media posts from Pakistani brands across five platforms, exploring which content gets Pakistani audiences to engage.

## Project Overview

This project analyzes social media post data to understand:

- Which platform performs better
- Which content type gets more engagement (likes, shares, comments)
- Which topics and hashtags are popular
- What sentiment generates engagement
- Which day and time work best
- Which audience segment is most responsive
- What a Pakistani brand should post next

## Files

| File | Description |
| --- | --- |
| `pakistan_socialmedia.ipynb` | Full Jupyter notebook: data loading, cleaning, analysis, visualizations, and summary |
| `pakistan_social_media_posts.csv` | Raw, uncleaned simulated dataset (3,030 rows, 17 columns) |
| `critique.md` | My check of the AI-generated 2-week marketing plan |

## Dataset

**Note: the dataset is simulated, so results demonstrate the method and are not evidence about real audience behaviour.**

- **Records:** 3,030 posts (before cleaning)
- **Platforms:** TikTok, Facebook, Instagram, YouTube, X (Twitter)
- **Cities:** Karachi, Lahore, Islamabad, Rawalpindi, Faisalabad, Peshawar, Quetta, Multan
- **Time range:** January 2024 to December 2024
- **Columns:** `post_id`, `timestamp`, `platform`, `brand_category`, `content_type`, `topic`, `caption`, `hashtags`, `language`, `city`, `audience_segment`, `followers_count`, `verified`, `likes`, `shares`, `comments`, `sentiment`

## Tools & Libraries

- Python
- Pandas, NumPy: data cleaning and manipulation
- Matplotlib, Seaborn: visualizations
- Jupyter Notebook

## Data Cleaning Steps

- Removed 30 duplicate rows
- Standardized inconsistent platform names (for example `tiktok` to `TikTok`)
- Corrected invalid values (negative likes)
- Filled missing hashtags and dropped rows with missing `followers_count`
- Converted `timestamp` to datetime
- Created derived features: `total_engagement`, `engagement_rate`, `day_of_week`, `hour`, `hashtag_count`, `follower_tier`

Engagement rate = (likes + shares + comments) / followers x 1,000. Results use the median.

## Visualizations Included

Bar plots (platform, content type, hashtags, sentiment, audience segment) and a day-by-hour heatmap.

## Key Insights

1. **TikTok drives the highest engagement** (39.2 per 1,000 followers for fashion posts), followed by Facebook (28.0). X (Twitter) is lowest (18.6).
2. **Short Video/Reel is the best content type** (42.4), but Live Stream is almost as strong (40.3).
3. **Cricket & PSL is the top topic** (48.3), ahead of Ramadan & Eid (37.6).
4. **Friday is the best day** (34.4), followed by Sunday (30.0) and Saturday (29.3).
5. **Hours 8pm to 11pm are nearly tied** (about 38 to 39), so an evening window works better than a single hour.
6. **AI-assisted plan:** I asked an AI for a 2-week posting plan for a Lahore clothing brand and checked it against my data. See `critique.md`.

## How to Run

1. Clone this repository or download the files.
2. Open `pakistan_socialmedia.ipynb` in Jupyter Notebook or Google Colab.
3. Place `pakistan_social_media_posts.csv` in the same directory as the notebook.
4. Run all cells in order.

## Author

Laiba Amin
