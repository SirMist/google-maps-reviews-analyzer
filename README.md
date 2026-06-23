[Google Maps Reviews Analyzer](https://apify.com/lone_neutrino/google-maps-reviews-analyzer?fpr=data)

# Google Maps Reviews Analyzer - AI-Powered Sentiment Analysis

Turn hundreds of Google Maps reviews into **actionable business insights** in minutes using AI.

This actor scrapes reviews from any Google Maps place and uses **AI (Gemini, GPT-4, or Claude)** to analyze sentiment, extract themes, and generate specific recommendations.

## What you get

For each place analyzed:

| Output | Description |
| --- | --- |
| **Overall sentiment score** | 0-100 score based on all reviews |
| **Positive themes** | What customers love most |
| **Negative themes** | Recurring complaints and issues |
| **Key recommendations** | Specific actions to improve ratings |
| **Response templates** | Ready-to-use replies for negative reviews |
| **Top reviews** | Most helpful positive and negative reviews |

## Use cases

1. **Business owners**: Understand what customers really think and where to improve
2. **Marketing agencies**: Audit client reputation before pitching services
3. **Competitive analysis**: Compare reviews across competitors in the same area
4. **Market research**: Analyze sentiment trends in an industry or region
5. **Local SEO**: Identify review patterns that affect search rankings

## Input

| Field | Type | Default | Description |
| --- | --- | --- | --- |
| `placeUrls` | string[] | required | Google Maps URLs or place IDs |
| `maxReviewsPerPlace` | number | 50 | Max reviews to analyze per place (1-500) |
| `llmProvider` | string | gemini | AI provider: `gemini`, `openai`, or `anthropic` |
| `apiKey` | string | required | API key for the selected LLM provider |
| `llmModel` | string | auto | Optional model override |
| `language` | string | en | Filter reviews by language (ISO code) |
| `proxyConfiguration` | object | none | Apify proxy settings |

## Example input

```
{
    "placeUrls": [
        "https://maps.google.com/?cid=1234567890",
        "https://www.google.com/maps/place/Restaurant+Example/@52.37,4.89"
    ],
    "maxReviewsPerPlace": 100,
    "llmProvider": "gemini",
    "apiKey": "your-gemini-api-key",
    "language": "en"
}
```

## Example output

```
{
    "placeName": "Restaurant Example",
    "totalReviewsAnalyzed": 87,
    "averageRating": 4.2,
    "sentimentScore": 78,
    "positiveThemes": [
        "Excellent food quality and fresh ingredients",
        "Friendly and attentive staff",
        "Beautiful interior and atmosphere"
    ],
    "negativeThemes": [
        "Long wait times during weekends",
        "Limited parking options",
        "Inconsistent portion sizes"
    ],
    "recommendations": [
        "Implement a reservation system to manage weekend crowds",
        "Add parking information to Google Maps listing",
        "Standardize portion sizes across menu items"
    ],
    "responseTemplates": [
        {
            "forTheme": "Long wait times",
            "template": "Thank you for your feedback! We've recently implemented a reservation system to reduce wait times..."
        }
    ]
}
```

## AI providers

| Provider | Model | Cost per 100 reviews | Speed |
| --- | --- | --- | --- |
| **Gemini** (recommended) | gemini-2.0-flash | ~$0.01 | Fast |
| OpenAI | gpt-4o-mini | ~$0.05 | Fast |
| Anthropic | claude-3-haiku | ~$0.03 | Fast |

Gemini Flash is free up to 15 requests/minute — best option for most users.

## Cost

Typical run: **$0.10-0.50** on Apify platform + minimal LLM API costs (often free with Gemini).

## Combine with other actors

1. Use **Google Maps Scraper** to find all businesses in an area
2. Run **Google Maps Reviews Analyzer** on each place
3. Use results for competitive analysis, reputation audits, or lead qualification