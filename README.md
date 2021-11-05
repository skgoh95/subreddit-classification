# Project 3: Natural Language Processing of Subreddit Posts
------------------------------------------------------------

## Executive Summary
Reddit is a social news, content, and discussions website. Posts are organised according to subject into user-created 'subreddits', which covers practically any topic imaginable. Members submit content (such as images, texts, and links) to subreddits. 

As a new investment company which has 2 main trading desks - one for traditional securities and another for cryptocurrency, reddit is a platform that piques our interest. The authentic daily discussions from the wide range of financial discussions, from financial news, to market data, and traditional securities in the Investing subreddit, to the blockchain technology and general sentiments for new coins in the CryptoCurrency subreddit, this raw conversations are what we intend to keep our eyes peeled on.

This project aims to automate the monitoring of reddit posts related to investing for new investing leads for both desks. Through this new leads and hot trends, I hope to filter this information to the specific trading desks. As such, I need a model to analyse and categorise the reddit posts for further review & investigation by either the securities or crypto trading desks. The prediction will be made with the best logistic regression model or Multinomial Naive Bayes Classifier, with Count Vectoriser or TF-IDF Vectoriser, as evaluated by F1 score, Sensitivity, Specificity and Accuracy. 

4 models were evaluated, namely Logistic Regression (Count Vectoriser), Logistic Regression (TF-IDF Vectoriser), Multinomial Naive Bayes Classifier (Count Vectoriser) and Multinomial Naive Bayes Classifier(TF-IDF Vectoriser). The entire dataset was split into a training dataset and a testing dataset. Logistic Regression (TF-IDF Vectoriser) is preferred as compared to the other 3 models. Two reasons for this: maximization of focus metric, and best overall balance in our 4 metrics. Our focus metric, specificity, performed best in a logistic regression. The highest specificity is desired in the models. In addition, the logistic regression scores over 90% on 3 out of 4 metrics, while specificity scores a hair below 90%, at 89.9%.

## Background
Reddit is a social news, content, and discussions website. Posts are organised according to subject into user-created 'subreddits', which covers practically any topic imaginable. Members submit content (such as images, texts, and links) to subreddits.

As a new investment company which has 2 main trading desks - one for traditional securities and another for cryptocurrency, reddit is a platform that piques our interest. The authentic daily discussions from the wide range of financial discussions, from financial news, to market data, and traditional securities in the Investing subreddit, to the blockchain technology and general sentiments for new coins in the CryptoCurrency subreddit, this raw conversations are what we intend to keep our eyes peeled on.

## Problem Statement
This project aims to automate the monitoring of reddit posts related to investing for new investing leads for both desks. Through this new leads and hot trends, I hope to filter this information to the specific trading desks. As such, I need a model to analyse and categorise the reddit posts for further review & investigation by either the securities or crypto trading desks. The prediction will be made with the best logistic regression model or Multinomial Naive Bayes Classifier, with Count Vectoriser or TF-IDF Vectoriser, as evaluated by F1 score, Sensitivity, Specificity and Accuracy.

## Conclusion

I conclude by stating our findings, and providing a recommendation based on my company's requirement.

In comparing parameters, I find that a higher parameter number does not automatically translate to a better result. This is due to the diminishing returns in predictive power of the parameters. Also, using an ngram range is better than using singular words only. This is because focus words often come in a phrase, similar to why supermarkets place soft drinks next to pizzas, or why casket-sellers also sell flowers. In all three cases, things which complement one another are often used consecutively.

In comparing models, a TF-IDF vectorized model provides a better predictive value than a Count Vectorized model. This is because while some stop words have been removed, there are still many stop words prevalent in the dataset. TF-IDF balances out the frequency of words used by penalizing common words which are not explicitly found in our stop words. This provides a higher weightage for non-stop words. Among the non-stop words, some of these are focus words used in the different subreddits due to their different focus.

In comparing our two best models, logistic regression model is preferred as compared to our naive bayes model. Two reasons for this: maximization of focus metric, and best overall balance in our 4 metrics. Our focus metric, specificity, performed best in a logistic regression. The highest specificity is desired in the models. In addition, the logistic regression scores over 90% on 3 out of 4 metrics, while specificity scores a hair below 90%, at 89.9%. Our naive bayes performed slightly poorly of 88%+ on sensitivity, but impressively for specificity and precision (93.4% and 93.2% respectively). As such, while an equally weighted result points to using a naive bayes model (93.8% vs 92.7%), I believe that a logistic regression would be more reliable overall.

## Recommendations
I recommend using our logistic regression model for reasons provided above. To improve our model, I suggest a few things that I can do in the future:

1. Expand data collection from other sources (not just Reddit).
2. Identifying more stop words to reduce noise in our data.
3. Creating a dictionary to process words more appropriately.
4. Obtain greater computing power or more time to process a greater number of hyperparameters.