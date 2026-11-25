Project Report
This report explains what this project is about, what we did, and what we learned in simple, everyday language.

The Goal
People talk a lot about politics on social media (like Twitter). We wanted to see if a computer could read tweets about Kenyan politicians (like Uhuru Kenyatta and William Ruto) and automatically tell if the person writing the tweet was feeling Happy (Positive), Angry/Upset (Negative), or just Stating Facts (Neutral).

What Did We Do? (Step-by-Step)
Collected the Tweets: We started with a big pile of over 11,000 tweets.
Cleaned Up the Text: Just like washing vegetables before cooking, we cleaned the tweets by removing messy things that don't help us find feelings. We removed web links (URLs), tags (like @username), numbers, and punctuation.
Labeled the Feelings: We took 1,000 tweets and used an automated tool called VADER to tag each tweet as either Positive, Neutral, or Negative.
Taught the Computers: We split these 1,000 tweets. We showed 800 of them to two different computer programs (our models) so they could learn which words are usually positive (like "good", "love") and which are negative (like "corrupt", "failed").
Tested the Models: We gave the remaining 200 tweets to our models to see if they could guess the correct feelings without looking at the answers.
The Final Results:
We tested two computer models:

Model 1: Naive Bayes (The "Optimistic" Model)
Grade: 54.5% score on the test.
What it did: It was too optimistic. It kept guessing that angry/negative tweets were actually positive because it struggled to understand negative tones.
Model 2: Logistic Regression (The "Balanced" Winner) 
Grade: 58.5% score on the test.
What it did: This model did a much better job. It was more balanced and was able to spot angry, neutral, and happy tweets much more evenly.
Important Things to Keep in Mind (Limitations)
Language Barriers: People in Kenya often speak Swahili or Sheng (slang), or use sarcasm. Because our computer tools are mostly trained on plain English, they sometimes missed the real meaning of these tweets.
Not the Whole Country: Twitter users are usually younger or live in cities, so these results don't represent what every person in Kenya thinks.
