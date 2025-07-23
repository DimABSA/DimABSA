# SemEval-2026 Task: Dimensional Aspect-Based Sentiment Analysis (DimABSA)

## Overview

Aspect-Based Sentiment Analysis (ABSA) aims to identify specific aspects or targets within a text and determine the corresponding sentiment polarity, traditionally using discrete categories such as positive, negative, or neutral (Pontiki et al., 2014; 2015; 2016). While this categorical approach has dominated ABSA research, it falls to capture the nuanced emotional gradations present in human language. To address this limitation, we introduce a new task called Dimensional ABSA (DimABSA). Unlike conventional ABSA, DimABSA requires systems to predict continuous real-valued scores representing valence (emotional positivity or negativity) and arousal (intensity of emotion) for each relevant aspect in a given text. This finer-grained, dimensional sentiment representation enables a deeper understanding of emotional subtleties, supporting a wide range of applications, including misinformation detection (Liu et al., 2024; Yun et al., 2024), mental health inference (Larson et al., 2013; Teodorescu et al., 2023), emotion dynamics in dialogue systems (Hipson & Mohammad, 2021), empathetic and personalized response generation (Wen et al., 2024), and stance detection (Upadhyaya et al., 2023; Shiwakoti et al., 2024).


## Subtasks

Participants can choose to participate in one or more subtasks:

### 1. Dimensional Aspect Sentiment Regression (DimASR)

Given a textual instance and one or more target aspects, predict a real-valued valence-arousal (VA) score for each aspect


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
