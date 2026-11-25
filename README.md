Project Presentation Report
1. Project Title
Sentiment Analysis of Kenyan Political Discussions: A Machine Learning Approach

2. Executive Summary
Objective:
Analyze public sentiment regarding political figures (Uhuru Kenyatta & William Ruto) in Kenya using Twitter data.
Methodology:
Collected and cleaned over 11,000 tweets, annotated a representative sample of 1,000 tweets using VADER, and compared Multinomial Naive Bayes against Logistic Regression using a TF-IDF vectorization pipeline.
Key Finding:
Logistic Regression outperformed Multinomial Naive Bayes, achieving a higher accuracy of 58.50% and a more balanced classification performance across all sentiment classes.
4. Data & Preprocessing Pipeline
Initial Dataset: 11,723 raw records.
Cleaned Dataset: 11,569 high-quality tweets.
Preprocessing Steps:
Removed missing tweet texts and duplicated records.
Lowercased all text to achieve standard casing.
Stripped non-informative elements (URLs, @mentions, and numeric characters).
Cleaned special punctuation/emojis while preserving essential spaces.
Removed empty records resulting from the cleaning process.
5. Modeling & Strategy
Sampling: Stratified 80/20 split on 1,000 VADER-annotated samples (800 Train / 200 Test) to ensure class distribution consistency.
Features: TF-IDF (Term Frequency-Inverse Document Frequency) word vectorizer pipeline.
Models Tested:
Multinomial Naive Bayes (Generative model base)
Logistic Regression (Discriminative linear model)
6. Comparative Evaluation Results
Evaluation Metric	Naive Bayes	Logistic Regression (Winner)
Accuracy	54.50%	58.50%
Weighted Precision	61.90%	58.44%
Weighted Recall	54.50%	58.50%
Weighted F1-score	52.27%	57.79%
Critical Takeaways from Confusion Matrices:
Naive Bayes struggled significantly with the negative class (only predicting 25% recall), showing a high bias toward predicting "positive" labelings.
Logistic Regression demonstrated a much more stable and balanced performance, maintaining a balanced distribution of correct predictions across positive, negative, and neutral classes.
7. Challenges & Ethical Considerations
Language & Cultural Nuances: Political discourse in Kenya heavily utilizes Swahili, Sheng, and local sarcasms which English-trained lexicon-lexicons (like VADER) may mislabel during auto-annotation.
Platform Representation Bias: Twitter users represent a specific demographic subsection of Kenya and may not reflect the political opinions of the wider, offline Kenyan public.
8. Future Directions
Fine-Tuning Semantic Context: Replace VADER with native multilingual models (such as AfroXML-RoBERTa or Swahili-BERT) to capture Kenyan linguistic contexts.
Hyperparameter Optimization: Conduct grid searches to optimize tokenization parameters and regularizations in Logistic Regression.
