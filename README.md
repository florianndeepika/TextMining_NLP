# Sentiment Analysis on Volkswagen Diesel Emission scandal and Crisis Management using BERT and Word Embedding

## Executive Summary : 
  Volkswagen (VW), world's most prominent auto manufacturer caught public attention in 2015 for an emission scandal called Dieselgate. There were multiple headline news came to limelight from 2015 to 2019. People were rambling on throwing out views about the scandal on the social media. The scandal and the series of events followed after the crisis made VW to give up their remarkable marketing slogan ‘Das Auto’. The purpose of this study is to analyze the trend in public opinion during this crisis. Automobile industry crisis and environment are the two main themes taken for this
research with sentiment analysis using Rapidminer and BERT model.

  The study focuses on one of the crisis management strategies, the goodwill package provided by VW to gain back their customer confidence. Sentiment analysis was performed on Twitter dataset using BERT. Surprisingly, about 60% of the sentiment extracted from BERT was negative which depicts that albeit measures were taken by the organization to regain their brand name and customers, it was not well received by the VW loyalists. Additionally, word embedding was performed to understand the word representation of the corpus. Three word embedding algorithms were
applied and comparison of the model was performed. It was observed that training word embedding with high dimension results in high accuracy of similar word representation. Finally, the study concludes that the goodwillpackage alone was not sufficient to manage the crisis. Instead, VW could have taken additional measures by addressing customer expectations at the right time.

## Analysis:
The study focuses on the crisis management strategy [14] adopted by Volkswagen to handle the most complicated emission scandal of their entire history. The aim of this part is to examine whether goodwill package offered by the organization to gain back their reputation received a positive or negative feedback from public. Two different perspectives were taken on the data. Firstly, sentiment was extracted from tweets using BERT [15]. Secondly, word embedding was performed with 3 techniques to understand word representation in a vector space [22].

**Sample, data, corpus**
To examine the effectiveness of goodwillpackage and perception of people requires sufficient data. Twitter data with 3253 tweets were collected under the hashtags #goodwillpackage and #vwcares. Worldwide data was taken which was limited to English tweets.

**Extraction Process:**
Snscrape python package was used to access the twitter API for tweet data extraction. TwitterSearchScraper method from snscrape package accepts query with relevant input parameter like language preference with date and needed hashtag or text. It provided tweets, username and date matching the query as output.

**Descriptive Statistics**
Total number of tweets used for the analysis were 3253 under hashtags: #goodwillpackage and #vwcares. Sentiment analysis was performed taking into consideration of the following factors from the tweets,
  
1. Opinion Holder -> Public and car owners.
2. Object -> Goodwill package provided by the company

## Main Analysis, Methodology
An empirical analysis was performed by researching the communication happened in twitter during the corporate crisis calls to determine whether tweets conveyed a positive or negative opinion about the topic. This was studied by performing sentiment analysis to analyze the effect of the goodwill package provided by Volkswagen. Sentiments were extracted from the tweets using BERT [17]. Additionally, Word embedding was performed with 3 techniques namely, Embedding layer, GloVe (Global Vector for Word Representation) and high dimension word embedding [16].

**Sentiment Analysis with BERT**
Sentiment analysis determines the attitudes, opinions, views, and emotions of people through Natural Language Processing (NLP) techniques. It involves classifying opinions in tweets into categories namely "positive" or "negative" or "neutral". BERT (Bidirectional Encoder Representations from Transformers) is a machine Learning model used in NLP. BERT [18] model uses transformer to understand the context and ambiguity in a language. Transformers allows to use a pre- trained BERT neural network to extract sentiment with 3 attributes negative sentiment (1 & 2), neutral (3) and positive sentiment (4 & 5).

<img width="978" alt="image" src="https://user-images.githubusercontent.com/63796480/175787719-110a6532-e65f-428a-9385-151773352607.png">

BERT leverages advanced NLP to calculate sentiment from the Twitter dataset. Figure 26 depicts the strength values of the sentiment extracted using BERT. Figure 27 shows three attributes of the sentiments extracted with Negative: 1914 tweets, Positive: 1139 tweets, Neutral: 200 tweets. Negative tweets seem to overshadow the positive comments despite the organization coming up with a management strategy.
Word Embedding for Sentiment Analysis:
Word Embedding is a traditional method of language processing which represent words in a numerical way or vector. This approach builds a word embedding space, which captures relationship between similar words by measuring syntactic and semantic similarities [25] between words where each word is positioned into a multi-dimensional space. This research work focuses on three word embedding techniques [28].

<img width="1006" alt="image" src="https://user-images.githubusercontent.com/63796480/175787738-d7424fe9-1399-42c1-b98a-ef94078cf96d.png">

Nltk and Keras were the two packages used. An Embedding layer of Keras was used to create word embeddings from the training data.

**Data preparation:** The extracted tweets were already cleaned by pre-processing steps by removing URL, punctuations, numbers and stop words.
**Train test split:** Data was split into train and test data in the ratio of 70:30
**Convert words into integers:** The words in the corpus were converted into number using Tokenization (Figure 29).
**Word sequences of equal length:** Before performing word embeddings, care was taken to make sure the sequences of words are in equal length by checking the maximum length of the tweets to avoid losing information as the tweets are rather short. Encoding the target variable: Sentiments extracted were Label Encoded for further analysis.

## Modelling:
Method 1: Training word embeddings using Embedding layer
Figure 29: Word frequency after Tokenization
Keras was used to create Embedding layer [28] to convert each word into a multi-dimensional vector for vector representation of words. Validation accuracy received was 60% which is relatively good because of our data size. Test accuracy obtained was 56.45 % which looks quite good with our small corpus. This can be still improved by using pre- trained word embeddings.
Method 2: Pre-trained word embeddings — GloVe
The dataset used in this paper is quite small which might affect the performance of the model. Therefore, GloVe which has multiple pre-trained word embeddings on a much larger training data. After running the model Validation accuracy was 65% with test accuracy of 58.30% which has increased relatively.
Method 3: Training word embeddings with more dimensions
The same data is used with high dimension and the accuracy of the test data is increasing. Validation accuracy was
83% with test accuracy of 65.16%. Accuracy of each models with its train and validation loss is provided in table 4.

<img width="968" alt="image" src="https://user-images.githubusercontent.com/63796480/175787778-dfae74ab-1272-4248-b6db-9b86d0dee7db.png">

## Results
The study reveals that the sentiment analysis performed on the communication about goodwill package is characterized by negative opinions. Volkswagen’s tweets were not able to reduce the emotionality and sentiment of the ongoing Twitter discussion. The communication remained negative, albeit customers being provided with compensations. Accusation and distrust about the way package delivered could have been one of the major causes for negative opinions. It was felt that the company was not being fully transparent and not ‘owning’ the problems. On the word embedding, the model provides better results in higher dimensions. The model can even outperform if it was trained on a much larger Twitter corpus.

## Conclusion, Limitations and Outlook

**Conclusion**
The dieselgate is one of the most expensive business crisis with unprecedented global scope and social media outcry. By examining the sentiment analysis, it was found that the negative sentiments prevailed throughout the 3 years analysis reflects customers anger on the company and concerns over the vehicles. Moreover, the goodwill package announced amid Volkswagen emission lawsuits, did not seem to work well. Volkswagen tried to create a positive gesture toward its customers who were waiting for an answer from the automaker regarding their vehicles. However, the scandal had devastated the owners making them angry which prevailed even after company announced goodwill package. Finally, though dieselgate had detrimental effect on the environment, tweets exchanged during the scandal shows that people concern was more on their cars being reported under scandal and the organization cheating them more than environment being polluted.

**Recommendation**
Managing customer perception is the key to business success. Considering this to be one of the most significant crisis
in the automobile industry costing over 30 billion Euros [6], the following recommendations are put forth to overcome such events,
• Organization must be transparent with their customers when unexpected events happen
• Effective communication is vital by keeping customers informed and responding them on time
• Establishing a right crisis management approach with proper and timely communication can develop the trust
in people
• Setting up a dedicated crisis management team ahead of time
• Maintaining a social media crisis team with effective online presence to address customer issues will favor
maintaining the e-reputation during negative event

**Limitation**
Small corpus is the major limitation for this study. Tweets restricted only to English language was considered for the sentiment analysis which might not produce the overall picture of the scandal.
