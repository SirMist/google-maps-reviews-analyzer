[Google Maps Reviews Analyzer](https://apify.com/strange-advanced-marketing/google-maps-reviews-analyzer?fpr=data)

Scrape and analyze Google Maps reviews for any business or search query. Get individual reviews with ratings, dates, and full text, plus AI-powered sentiment analysis, theme detection, and actionable insights.

## What It Does

1. **Scrapes Reviews** — Extracts reviewer name, rating, date, full review text, and business owner responses
2. **Analyzes Sentiment** — Scores each review from -1 (negative) to +1 (positive) using keyword analysis
3. **Detects Themes** — Identifies what reviewers talk about: pricing, service quality, timeliness, cleanliness, reliability
4. **Extracts Keywords** — Finds the most common words in positive and negative reviews separately
5. **Flags Red Flags** — Highlights 1-2 star reviews for immediate attention
6. **Rating Distribution** — Shows the breakdown of star ratings

## Use Cases

- **Reputation Monitoring** — Track what customers say about your business
- **Competitor Analysis** — Compare review sentiment across competitors
- **Local SEO** — Identify themes that drive positive reviews
- **Marketing Agencies** — Audit client reputation before onboarding
- **Lead Generation** — Find businesses with poor reviews (they need help!)

## Input Options

| Field | Description | Default |
| --- | --- | --- |
| searchQuery | Google Maps search or direct place URL | Required |
| maxBusinesses | How many businesses to analyze | 5 |
| maxReviewsPerBusiness | Reviews to scrape per business | 50 |
| minRating | Only include businesses above this rating | 1 |
| sortBy | Sort reviews: newest, highest, lowest, relevant | newest |
| analyzeSentiment | Run sentiment & theme analysis | true |

## Output

Each business includes:

- Basic info (name, rating, review count, address, phone)
- Individual reviews with sentiment scores and themes
- Analysis summary with:

- Average sentiment score
- Positive/negative/neutral review counts
- Rating distribution
- Top themes mentioned
- Most common keywords (overall, positive, negative)
- Red flag samples (worst reviews)

## Built By

**Strange Advanced Marketing (S.A.M.)** — AI-powered marketing for trade contractors.

Also check out our other tools:

- [Google Maps Lead Generator](https://apify.com/strange-advanced-marketing/google-maps-lead-generator) — Find leads with email & social enrichment
- [Instagram Profile Scraper](https://apify.com/strange-advanced-marketing/instagram-profile-scraper)
- [TikTok Profile Scraper](https://apify.com/strange-advanced-marketing/tiktok-profile-scraper)
- [Business Website Analyzer](https://apify.com/strange-advanced-marketing/business-website-analyzer)