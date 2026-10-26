# Customer Review Analytics

Customer review analytics project developed during my **Business Data Analyst internship at Auto2000** to support the monitoring and analysis of Google Maps customer reviews across multiple branches.

The project combines **data collection, text preprocessing, sentiment classification, review categorization, aspect-based analysis, and Power BI visualization** to transform unstructured customer reviews into actionable information.

## Project Overview

Customer reviews on Google Maps contain valuable information about customer experiences, service quality, facilities, sales interactions, and aftersales services. However, manually reviewing a large number of customer comments can be time-consuming and makes cross-branch monitoring difficult.

This project was developed to create a more structured workflow for processing and analyzing customer reviews and presenting the results through an interactive dashboard.

The final dashboard covered **7 branches** and enabled both individual branch analysis and cross-branch comparison.

## Objectives

The project aimed to:

- Process and structure Google Maps customer review data.
- Classify customer sentiment into positive, negative, and neutral categories.
- Categorize reviews into Sales, Aftersales, and Other.
- Identify multiple service aspects discussed within each review.
- Monitor review trends, ratings, sentiment, and customer feedback through Power BI.
- Support comparison of customer review patterns across branches.

## Workflow

The project followed the general workflow:

**Google Maps Reviews → Apify → Google Sheets → Python / Google Colab → Sentiment & Aspect Analysis → Google Sheets Output → Power BI Dashboard**

Reviews from each branch were processed using the same analytical workflow before being used for branch-level and cross-branch reporting.

## Data Processing

The text preprocessing pipeline included:

- Lowercase conversion
- Unicode normalization
- Typo correction
- Repeated-character normalization
- Emoji and symbol cleaning
- Slang normalization
- Stopword removal
- Text filtering

The public repository does not include the original customer review dataset, internal spreadsheet connections, credentials, or proprietary files.

## Sentiment Analysis

Sentiment classification was performed using a **pre-trained TF-IDF vectorizer and XGBoost classification model**.

The initial model predictions were further supported by rule-based sentiment refinement using positive and negative keywords.

Sentiment classes:

- Positive
- Negative
- Neutral

For one documented branch execution, the processing pipeline started with **1,000 scraped reviews**, with **628 reviews retained after text availability checks and preprocessing**.

## Review Categorization

Customer reviews were categorized into:

- **Sales**
- **Aftersales**
- **Other**

The categorization process used keyword-based rules designed around the business context of automotive sales and aftersales services.

## Aspect-Based Analysis

Each review could contain multiple customer experience aspects.

The analyzed aspects included:

- Sales
- Booking
- Facilities
- Technician
- Price
- Waiting Time
- Spare Parts
- Service Advisor

Up to three relevant aspects could be assigned to a review based on keyword matching.

The aspect results were also transformed into a flattened structure to support multi-aspect analysis in Power BI.

## Dashboard

The Power BI dashboard consisted of two main analytical views:

### Branch Analysis

Provides detailed monitoring for an individual branch, including:

- Total reviews
- Sentiment distribution
- Sentiment by service aspect
- Rating distribution
- Review trends
- Review categories
- Reviews containing photos
- Customer review text

### Branch Comparison

Supports comparison across 7 branches based on:

- Review volume
- Rating distribution
- Sentiment distribution
- Review categories
- Service aspects

## Tools & Technologies

- **Python**
- **Pandas**
- **Scikit-learn**
- **XGBoost**
- **TF-IDF**
- **Google Colab**
- **Google Sheets**
- **Apify**
- **Power BI**

## Repository Contents

```text
customer-review-analytics/
├── README.md
├── customer_review_analytics.ipynb
└── requirements.txt
```

## Notes

This repository is a portfolio documentation of a project completed during my internship at Auto2000.

Original customer datasets, credentials, internal spreadsheet connections, proprietary model files, and personally identifiable information are not included in this public repository.
