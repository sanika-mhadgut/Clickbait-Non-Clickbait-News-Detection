# Clickbait-Non-Clickbait-News-Detection

Clickbait is a term used to describe content, typically in online media, that is designed to attract attention and encourage users to click on a link, often with the goal of generating page views and advertising revenue. 
Clickbait relies on sensationalism, exaggeration, or misleading information to entice users to click through to the content.
The catch is that the content behind the click often doesn't live up to the excitement they create.
Clickbait can be frustrating because it makes people feel misled and disappointed. It erodes trust because the content doesn't match the promises made in the headlines.
Since, trust is crucial online, just like in any relationship. If a website can't be trusted, people might not want to rely on it for information.
As a result, there's a growing interest in developing tools and techniques, such as machine learning models, to detect and mitigate the impact of clickbait in online spaces

Utilize EDA techniques for a comprehensive exploration of the dataset.
Apply statistical analyses to quantify differences, focusing on word frequency, sentiment, and headline length.
Identify predominant distinctions between clickbait and non-clickbait, emphasizing emotional tone, linguistic and structural characteristics.
Employed feature engineering to identify and create new feature
Train machine learning models, refining them iteratively for accuracy improvement.
Compared the performance of the models with and without feature engineering

Dataset size: 32,000 headlines.
Well-balanced distribution between clickbait and non-clickbait examples.
Gathered from popular sites such as 'BuzzFeed,' 'Upworthy,' 'ViralNova,' 'Thatscoop,' 'Scoopwhoop,' and 'ViralStories.'
Collected from reputable news sources like 'WikiNews,' 'New York Times,' 'The Guardian,' and 'The Hindu.'
Testing Data : Extracted from reliable news websites such as 'Fox News' and 'BBC.'
Testing Data : Scraped from 'BuzzFeed' to create a diverse testing set.

Average Length: Clickbait headlines tend to be slightly longer on average (55.74 characters) compared to non-clickbait headlines (51.85 characters).
Variability: Clickbait headlines have a slightly higher variability in length (as indicated by the standard deviation) compared to non-clickbait headlines. This suggests that the length of clickbait headlines varies more widely than non-clickbait headlines.
Minimum and Maximum Length: Clickbait headlines have a minimum length of 6 characters and a maximum length of 125 characters, while non-clickbait headlines have a minimum length of 11 characters and a maximum length of 135 characters. This indicates that there is a wide range of headline lengths for both categories.



Noun Usage:
Clickbait: Demonstrates a higher frequency of impactful and sensational nouns, often related to trending topics or celebrities. It focuses more on proper nouns.
Non-Clickbait: Exhibits a balanced use of nouns, maintaining a focus on factual and informative language related to news events or topics.
Adjective Usage:
Clickbait: Displays an increased prevalence of extreme adjectives (e.g., best, most) to evoke emotions and create urgency.
Non-Clickbait: Uses adjectives more conservatively, contributing to context and clarity in a measured tone.
Verb Usage:
Clickbait: Features a higher occurrence of dynamic verbs (e.g., guess, remember) emphasizing action and engagement.
Non-Clickbait: Uses verbs straightforwardly (e.g., arrested, killed) for factual reporting, contributing to clarity without exaggerated urgency.


NER Patterns in Clickbait:
Clickbait headlines often emphasize named entities related to celebrities, entertainment, and sensational topics to attract attention and engage emotionally.
NER Patterns in Non-Clickbait:
Non-clickbait headlines tend to focus on named entities associated with countries, politics, and global events, prioritizing factual reporting and an objective tone.
Content Focus and Audience Appeal:
The use of different named entities reflects the distinct content focus and target audience of clickbait (emotionally engaging) and non-clickbait (informative reporting).
Clickbait NER Patterns - Entity Focus on Person:
In clickbait headlines, the Named Entity Recognition (NER) patterns emphasize entities related to individuals, particularly focusing on celebrities and personalities to create engaging and attention-grabbing content.

Clickbait NER Patterns - Entity Focus on Person:
In clickbait headlines, the Named Entity Recognition (NER) patterns emphasize entities related to individuals, particularly focusing on celebrities and personalities to create engaging and attention-grabbing content.
Non-Clickbait NER Patterns - Entity Focus on GPE (Geo-Political Entities):
Non-clickbait headlines tend to center their NER patterns around Geo-Political Entities (GPE), emphasizing countries, political regions, and global locations. This reflects a focus on informative reporting and a more neutral tone.
Content Tone and Emphasis:
Clickbait leverages person-centric entities for emotional engagement, while non-clickbait employs GPE entities for factual reporting and a more objective presentation of information.

Incorporated four new features - ‘contains_personal_pronouns’, ‘contains_numbers’, ‘contains_gpe’ and ‘sentiment_scores’
‘contains_personal_pronouns’, ‘contains_numbers’, and ‘sentiment_scores’ are highly correlated with label
‘contains_gpe’ is evident in non clickbait headlines which acts as a distinguishing feature

Clickbait TF-IDF Words: The identified words suggest common themes in clickbait headlines, including enticing actions ("make," "know"), time-related elements ("time"), and a sense of urgency ("need," "best").
Non-Clickbait TF-IDF Words: The non-clickbait words indicate different themes, such as negative events ("kill," "dy," "dead"), news-related terms ("new," "say," "president"), and location-specific terms ("uk," "australian").


Clickbait N-grams:
Clickbait headlines frequently contain phrases like "here be," "you be," and "you will," suggesting a personalized and engaging tone.
The mention of "zodiac sign" and "base zodiac" indicates a common theme related to astrological content.
The presence of "look like" and "what be" suggests content designed to evoke curiosity and encourage clicks.
Cultural references such as "harry potter" are also prominent, aligning with popular culture interests.

Non-Clickbait N-grams:
Non-clickbait headlines often include location-based phrases like "new york" and "new zealand," indicating a focus on news and events in specific regions.
References to interviews, as seen in "wikinews interview," suggest informative and journalistic content.
Geopolitical terms like "north korea" and "prime minister" reflect a focus on global affairs.
The mention of events like "plane crash" and "world cup" aligns with news and sports-related content.


Average Sentiment: Clickbait headlines, on average, have a slightly positive sentiment (0.1068), while non-clickbait headlines have a slightly negative average sentiment (-0.1071).
Similar Variability: Both clickbait and non-clickbait headlines show a similar level of variability in sentiment scores, as indicated by the standard deviation.
Minimum and Maximum Sentiment: Clickbait headlines have a minimum sentiment score of -0.9274 and a maximum of 0.9413. Non-clickbait headlines have a minimum sentiment score of -0.9485 and a maximum of 0.9287. This indicates that sentiment scores for both categories cover a wide range, and there is no clear dominance of positive or negative sentiment in either category.

Conducted statistical t-tests to determine if there are significant differences in linguistic features between clickbait and non-clickbait headlines.
The t-statistic measures how many standard deviations the sample mean of the group differs from the population mean. 
The p-value is the probability of observing such an extreme t-statistic if the null hypothesis were true (i.e., there is no difference between groups). 

Results: The t-statistic is quite large (35.79), suggesting a substantial difference in average sentence length between two groups.

With a p-value close to zero, we reject the null hypothesis. (i.e., there is no difference between groups)
Therefore, there is strong evidence that the average sentence lengths are significantly different between clickbait and non-clickbait headlines.



The lower scores for clickbait headlines in all three metrics (Flesch-Kincaid, Gunning Fog, and Coleman-Liau)
Indicates that clickbait headlines tend to use simpler language and are generally more readable
Performed Statistical T-test. 
Statistically significant difference in Flesch-Kincaid Grade Level :  1.5374670487129924e-162

Removed rows with missing values.
Label Encoding: Converted categorical bias labels to numeric values.
POS Tagging for Lemmatization:
Converted text to lowercase.
Removed punctuation and digits.


Removed stop words.
Use BeautifulSoup to handle HTML entities.
Fixed contractions and handle specific substitutions.
Lemmatized words using WordNetLemmatizer.
Tokenized the cleaned text.



Word Embedding - Tfidfvectorizer
Logistic Regression
Multinomial Naive Bayes
Random Forest


Logistic Regression:
Baseline (Before Feature Engineering): 56.4% accuracy.
After Feature Engineering: 82.81% accuracy.
Random Forest:
Baseline (Before Feature Engineering): 83% accuracy.
After Feature Engineering: 87.01% accuracy.
Multinomial Naive Bayes:
Baseline (Before Feature Engineering): 68% accuracy.
After Feature Engineering: 84.56% accuracy.

