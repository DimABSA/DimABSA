# SemEval-2026 Task: Dimensional Aspect-Based Sentiment Analysis (DimABSA)

## Overview

Aspect-Based Sentiment Analysis (ABSA) is an NLP task focused on identifying aspect terms and associated sentiment polarity within text. Following the success of previous SemEval ABSA tasks, Dimensional ABSA (DimABSA) introduces a novel sentiment representation using fine-grained, real-valued scores of valence (negative to positive) and arousal (low to high excitement), inspired by psychological theories.

## Task Features

* Utilizes real-valued valence and arousal scores for nuanced sentiment analysis.
* Covers three distinct domains: customer reviews, financial reports, and stance detection.
* Includes datasets in 16 languages across diverse regions, both high-resource and low-resource.

## Subtasks

Participants can choose to participate in one or more subtasks:

### 1. Dimensional Aspect Sentiment Regression (DimASR)

Predict valence-arousal (VA) scores for specified aspects.

**Example Input:**

```json
{
  "ID": "001",
  "Text": "The food was delicious, but the service was terrible.",
  "Aspect": ["food", "service"]
}
```

**Example Output:**

```json
{
  "ID": "001",
  "Aspect_VA": [
    {"Aspect": "food", "VA": "8.50#7.20"},
    {"Aspect": "service", "VA": "2.00#6.80"}
  ]
}
```

### 2. Dimensional Aspect Sentiment Triplet Extraction (DimASTE)

Extract triplets (aspect term, opinion term, valence-arousal score).

**Example Input:**

```json
{
  "ID": "002",
  "Text": "Battery life is excellent, but the screen is dull."
}
```

**Example Output:**

```json
{
  "ID": "002",
  "Triplet": [
    {"Aspect": "Battery life", "Opinion": "excellent", "VA": "8.80#7.00"},
    {"Aspect": "screen", "Opinion": "dull", "VA": "3.00#4.50"}
  ]
}
```

### 3. Dimensional Aspect Sentiment Quad Prediction (DimASQP)

Extract quadruplets (aspect term, aspect category, opinion term, valence-arousal score).

**Example Input:**

```json
{
  "ID": "003",
  "Text": "The hotel's location is great, but the rooms were dirty."
}
```

**Example Output:**

```json
{
  "ID": "003",
  "Quad": [
    {"Aspect": "location", "Category": "HOTEL#LOCATION", "Opinion": "great", "VA": "8.50#7.00"},
    {"Aspect": "rooms", "Category": "HOTEL#CLEANLINESS", "Opinion": "dirty", "VA": "2.20#5.80"}
  ]
}
```

## Languages Covered

* African: Emakhuwa, Hausa, Igbo, Kinyarwanda, Mozambican Portuguese, Swahili, Twi, Xhosa
* Asian: Chinese, Japanese
* European: English, German, Portuguese (Brazilian), Russian, Ukrainian, Tatar

## Domains

* Customer Reviews (Restaurants, Laptops, Hotels)
* Financial Reports
* Stance Detection (Environmental Issues)

## Important Dates

* **Data Release:** \[To Be Announced]
* **Evaluation Period:** \[To Be Announced]
* **Results Submission:** \[To Be Announced]
* **SemEval-2026 Workshop:** \[To Be Announced]

## Contact

For inquiries, please contact: \[Task Organizers' Contact Information]

## Organizers

\[List of Task Organizers and Affiliations]

## References

Detailed references are available in the task description document.
