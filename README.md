# SemEval-2026 Task: Dimensional Aspect-Based Sentiment Analysis (DimABSA)


Aspect-Based Sentiment Analysis (ABSA) aims to identify specific aspects or targets within a text and determine the corresponding sentiment polarity, traditionally using discrete categories such as positive, negative, or neutral (Pontiki et al., 2014; 2015; 2016). While this categorical approach has dominated ABSA research, it falls to capture the nuanced emotional gradations present in human language. 

To address this limitation, we introduce a new task called Dimensional ABSA (DimABSA). Unlike conventional ABSA, DimABSA requires systems to predict continuous real-valued scores representing valence (emotional positivity or negativity) and arousal (intensity of emotion) for each relevant aspect in a given text. This finer-grained, dimensional sentiment representation enables a deeper understanding of emotional subtleties, supporting a wide range of applications, including mental health inference (Larson et al., 2013; Teodorescu et al., 2023), emotion dynamics in dialogue systems (Hipson & Mohammad, 2021), empathetic and personalized response generation (Wen et al., 2024), and stance detection (Upadhyaya et al., 2023; Shiwakoti et al., 2024).


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

Given a textual instance, extract all triplets consisting of an aspect term, an opinion term, and a valence-arousal (VA) score.

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

Given a textual instance, extract all triplets consisting of an aspect term, an aspect category, an opinion term, and a valence-arousal (VA) score. This task is an extension of Subtask 2 (triplet extraction), with the addition of the aspect category element.

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




# Languages, Tracks and Domain

The table below lists the tracks and specifies the languages available in each track for the shared task. 


> Participants may choose to participate in one or more languages and tracks of their preference.


| No. | Language                | Code | Track A (DimASR)                    |  Track B( DimASTE)            |  Track C (DimASQP)            |
| --- | ----------------------- | ---- | -------------------------- | ------------------ | ------------------ |
| 1   | Chinese                 | ZHO  | Restaurant, Laptop         | Restaurant, Laptop | Restaurant, Laptop |
| 2   | English                 | ENG  | Restaurant, Laptop, Stance | Restaurant, Laptop | Restaurant, Laptop |
| 3   |                  |   |  |  |  |
| 4   |                  |   |  |  |  |



**Legend**:  
- **✓**: The language is supported for the specified track.
- **✗**: The language is not supported for the specified track.

* African: Emakhuwa, Hausa, Igbo, Kinyarwanda, Mozambican Portuguese, Swahili, Twi, Xhosa
* Asian: Chinese, Japanese
* European: English, German, Portuguese (Brazilian), Russian, Ukrainian, Tatar




# Evaluation

The performance of the submitted systems will be evaluated based on the following metrics:


- <b> Track A: Multilabel Emotion Detection</b> 
  The evaluation metric will be the  ...

- <b> Track B: Emotion Intensity</b> 
    The evaluation metric will be ...

- <b>Track C: Crosslingual Emotion Detection</b> 
  The evaluation metric will be ....

- For details about the evaluation script and the submission file format checker, check this [guide](#).


## Important Dates

# Important Dates and Task Phases


| Description                   | Deadline                                        |
|-------------------------------|------------------------------------------------|
| Sample Data Ready             |  \[To Be Announced]                               |
| Training Data Ready           | \[To Be Announced]                    |
| Evaluation Start              |  \[To Be Announced]                              |
| Evaluation End                |  \[To Be Announced]                            |
| System Description Paper Due  |  \[To Be Announced]                               |
| Notification to authors       |  \[To Be Announced]                                 |
| Camera ready due              |   \[To Be Announced]                                    |
| SemEval workshop 2025         |  \[To Be Announced]  |



# How to Participate

1. **Register**: Sign up on the CodaBench competition platform.
2. **Track**: Decide on the track(s) you want to participate in (Track A, B and/or C).
3. **Download**: Access to the datasets for each track will be provided in this repository.
4. **Develop**: Build your models using the provided data.
5. **Submit**: Submit your predictions on the CodaBench competition platform.

Please follow the guidelines shared [here](#). 




# Competition Rules and Terms
<details>
  <summary>1. Consent to Public Release of Scores</summary>
  <ul>
    <li>By submitting results, you consent to the public release of your scores on:
      <ul>
        <li>the competition website,</li>
        <li>at the designated workshop,</li>
        <li>in associated proceedings.</li>
      </ul>
    </li>
    <li>Task organizers have discretion over the release and choice of metrics.</li>
    <li>Scores may include:
      <ul>
        <li>automatic and manual quantitative judgments,</li>
        <li>qualitative judgments,</li>
        <li>other metrics as deemed appropriate.</li>
      </ul>
    </li>
  </ul>
</details>

<details>
  <summary>2. Score Release and Validity</summary>
  <ul>
    <li>Task organizers reserve the right to withhold scores for:
      <ul>
        <li>incomplete submissions,</li>
        <li>erroneous submissions,</li>
        <li>deceptive submissions,</li>
        <li>rule-violating submissions.</li>
      </ul>
    </li>
    <li>Inclusion of a submission's scores does not constitute endorsement.</li>
  </ul>
</details>

<details>
  <summary>3. Team Participation Rules</summary>
  <ul>
    <li>Participants may be involved in only one team.</li>
    <li>Exceptions may be granted with prior approval from organizers.</li>
  </ul>
</details>

<details>
  <summary>4. Account Management</summary>
  <ul>
    <li>Each team must create and use exactly one account on the designated platform.</li>
  </ul>
</details>

<details>
  <summary>5. Team Constitution</summary>
  <ul>
    <li>Team membership cannot be changed after the evaluation period begins.</li>
  </ul>
</details>

<details>
  <summary>6. Development Period Rules</summary>
  <ul>
    <li>Teams can submit up to 999 submissions.</li>
    <li>Results are visible only to the submitting team.</li>
    <li>Leaderboard is disabled.</li>
    <li>Warnings and errors are visible for each submission.</li>
  </ul>
</details>

<details>
  <summary>7. Evaluation Period Rules</summary>
  <ul>
    <li>The teams are contrained to make 3 submissions.</li>
    <li>Only the final submission will be considered official.</li>
    <li>Warnings and errors are visible for each submission.</li>
  </ul>
</details>

<details>
  <summary>8. Post-Competition</summary>
  <ul>
    <li>The gold labels will be released after the competition.</li>
    <li>The teams are encouraged to report results on all their system variants in their description paper.</li>
    <li>The official submission results must be clearly indicated.</li>
  </ul>
</details>

<details>
  <summary>9. Public Release of Submissions</summary>
  <ul>
    <li>Final team submissions may be made public after the evaluation period.</li>
  </ul>
</details>

<details>
  <summary>10. Disclaimer about the Datasets</summary>
  <ul>
    <li>Organizers and affiliated institutions provide no warranties on dataset correctness or completeness.</li>
    <li>They are not liable for dataset access or usage.</li>
  </ul>
</details>

<details>
  <summary>11. Peer Review Process</summary>
  <ul>
    <li>Each participant will review another team's system description paper.</li>
  </ul>
</details>

<details>
  <summary>12. Dataset Usage Restrictions</summary>
  <ul>
    <li>Datasets should only be used for scientific or research purposes.</li>
    <li>Any other use is explicitly prohibited.</li>
    <li>Datasets must not be redistributed or shared with third parties.</li>
    <li>Interested parties should be directed to the official website.</li>
  </ul>
</details>
<details>
  <summary>13. Final ranking</summary>
  <ul>
    <li>To be included in the official task ranking, you **MUST** submit a system description paper.</li>
  </ul>
</details>




#  Resources

2. [SemEval 2026 Shared Tasks](https://semeval.github.io/SemEval2026/tasks)
3. [Frequently Asked Questions about SemEval](https://semeval.github.io/faq.html)
4. [Paper Submission Requirements](https://semeval.github.io/paper-requirements.html)
5. [Guidelines for Writing Papers](https://semeval.github.io/system-paper-template.html)
6. [Paper style files](https://github.com/acl-org/acl-style-files)
7. Previous shared-tasks on ABSA  [List them]



# FAQs
<details>
  <summary>Do I have to participate in all languages for a given track?</summary>
  <ul>
    <li>No, you can participate in one or more languages.</li>
  </ul>
</details>

<details>
  <summary>How will you verify my submitted model?</summary>
  <ul>
    <li>To be included in the final team rankings of our shared task, it is mandatory for participants to submit a system description paper describing their approaches and methodologies in detail, therefore ensuring scientific integrity.</li>
  </ul>
</details>

<details>
  <summary>When will you release the gold labels?</summary>
  <ul>
    <li>For the dev set, the gold labels will be released when the evaluation phase starts and the gold labels for the different test sets will be released after the competition is over.</li>
  </ul>
</details>

<details>
  <summary>Can I use LLMs in the different tracks?</summary>
  <ul>
    <li>Yes.</li>
  </ul>
</details>
<details>
<summary>Can I use additional datasets (e.g, publicly provided ones from other sources)?</summary>
  <ul>
    <li>Yes. Please do cite them in the system description paper.</li>
  </ul>
</details>

<details>
  <summary>Will I be included in the final ranking if I do not write a system description paper?</summary>
  <ul>
    <li>No. You MUST write a system description paper to be included in the final ranking.</li>
  </ul>
</details>

<details>
  <summary>I have never written a system description paper. How can I write one?</summary>
  <ul>
    <li>We will have an online writing tutorial and share resources to help you write a system description paper.</li>
  </ul>
</details>

<details>
  <summary>Do I need to pay conference registration fees and/or attend SemEval for my paper to be published?</summary>
  <ul>
    <li>It is not required to attend the SemEval workshop for the paper to be published. You do not have to pay any registration fees if you do not attend the workshop. However, if you want to attend the workshop, you need to pay for attendance.</li>
  </ul>
</details>

<details>
  <summary> Our system did not perform very well, should I still write a system description paper? </summary>
 <ul>
    <li> We want to hear from **all** of you even if you did not outperform other systems!Write about the details of your system. (**Yes we want your insights from any negative results!**)</li>
  </ul>

</details>



# Dataset paper

We will soon release a dataset paper that describes the data collection, annotation process, and baseline experiments. This paper will provide additional details and information that will be useful for the task participants.



## Contact

For inquiries, please contact: \[Task Organizers' Contact Information]

We need to create Google group.

## Organizers

\[List of Task Organizers and Affiliations]

## References


