Introduction:
Sentiment analysis is a technique for examining text data to determine its sentiment. The aim is to automatically recognize and categorize opinions stated in the text to calculate overall emotion. Sentiment analysis techniques categorize them as positive, neutral, or negative.
Using machine learning and text analytics, algorithms can categorize sentences into positive, negative, and neutral categories. Many companies, including Amazon and Twitter, use this sentiment analysis to analyze customer reviews on their products, and they will improve based on these results.
we will analyze these texts and calculate sentiment scores for each of them. So we will use Vader and RoBERTa models to calculate polarity scores.
This project’s primary objective is to conduct sentiment analysis, determine the polarity scores of the texts, and understand the sentiment hidden in each one.

These reviews include information about the product and the user, ratings given by customers, and a plain text review. This dataset contains,

A total of 568,454 reviews
Reviews from Oct 1999 – Oct 2012
Reviews from 256,059 users
There are 260 users with more than 50 reviews on 74,258 products

Positivity is higher for higher Star Review.
Neutral is almost flat Less negative of a comment as star review becomes negative.
Vader is valuable in having the connection between the sentiment score of the text and it does relate to the actual rating of the review.

Step 2: Previous model scored each word indivually without a context. Human language depends more about context.
RoBERTa Pretrained Model picks on negative words that actually are sarcastic, or reated to other words which may be actally positive.
Transformer(Hugging Face Library) Model accounts for words but also the context related to other words.
Hugging face is a leader in one of these models in gathering them, making it easily available.

Compare Scores between model

Step 3: Combine and compare
5 star is purple
1 star is blue
Vader-Less confident in its predictions
Positive results are towards right
For Roberta is almost to the right, correlation between models can also be seen(hardly)
Very high scores for 5 stars and low incase of positive sentiment score.
Analyzing Wrongly Classified Texts
Even though most of the texts are classified correctly, there will still be some ambiguous, wrongly classified sentences. 
Sometimes they may sound positive, but in actuality, they are negative. 
Similarly, positive sentences sometimes sound like negative ones. Now we will see a few texts that our models wrongly classify.
In the first example, we took a text that was classified as positive by Roberta, but the customer rating is 1.
In the second example, we took a text that was classified as positive by Vader, but the customer rating is 1.
It’s a negative one, but the customer might sarcastically give a review mentioning it as a positive note. So model analyzed it as positive text.

The last two examples are the same. Both Vader and Roberta models classified it as negative text but rated it 5.
Here the customer actually loved the food but gave the review complaining about weight gain. So models are classified as negative.

Conclusion:
The use of transformers made it simpler than ever to model the link between words.

A vast amount of unstructured review texts are analyzed using sentiment analysis in order to extract people's thoughts and categorize them into sentiment classes.
Sentiment analysis is the result of the fusion of machine learning technology and human emotional interpretation.
VADER Strengths: VADER is a lexicon and rule-based sentiment analysis tool designed for social media text and informal language. It works well for texts with clear positive or negative sentiment, especially when dealing with short, simple phrases.
Limitations: VADER struggles with complex linguistic constructs, sarcasm, and domain-specific text.

Typical Accuracy: On benchmark datasets, VADER achieves around 60%-75% accuracy depending on the dataset and task. It’s best suited for quick and approximate sentiment classification rather than detailed analysis.
RoBERTa Strengths:
RoBERTa (Robustly Optimized BERT Pretraining Approach) is a state-of-the-art transformer model pre-trained on massive datasets.
It can understand nuanced contexts, domain-specific language, and complex sentence structures. Fine-tuning on a specific sentiment dataset often yields much higher performance. Limitations:
Requires more computational resources for both training and inference.

Typical Accuracy:
On benchmark datasets like SST-2 (Stanford Sentiment Treebank), RoBERTa can achieve 90%-95% accuracy after fine-tuning. Its performance is superior to lexicon-based methods like VADER, especially for longer or more complex texts.


